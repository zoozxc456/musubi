<script setup lang="ts">
import type { SelectMenuItem } from '@nuxt/ui';

const isOpen = defineModel<boolean>('open');

const form = reactive({
  name: '',
  phone: '',
  attendance: 'attending',
  diet: 'none',
  guests: 0,
  note: '',
});

const dietOptions = reactive<SelectMenuItem[]>([
  { label: '葷食 (No restrictions)', value: 'none' },
  { label: '蛋奶素 (Vegetarian)', value: 'vegetarian' },
  { label: '全素 (Vegan)', value: 'vegan' },
  { label: '不吃牛 (No Beef)', value: 'no-beef' },
]);

const isSubmitting = ref(false);
const onSubmit = async () => {
  isSubmitting.value = true;
  await new Promise((resolve) => setTimeout(resolve, 1500));

  alert(
    `感謝 ${form.name} 的回覆！\n出席: ${form.attendance}\n人數: ${
      1 + form.guests
    }`,
  );
  isSubmitting.value = false;
  isOpen.value = false;
};
</script>

<template>
  <UModal
    v-model:open="isOpen"
    :ui="{
      overlay: 'z-[90] bg-stone-900/50 backdrop-blur-sm',
      content:
        'z-[100] sm:max-w-md bg-white/95 backdrop-blur-xl ring-1 ring-stone-200 shadow-2xl',
    }"
  >
    <template #content
      ><div class="p-8">
        <div class="text-center mb-8">
          <h3 class="text-2xl font-serif text-stone-800 mb-2">RSVP</h3>
          <p class="text-xs tracking-widest text-stone-400 uppercase">
            Kindlly Respond
          </p>
        </div>

        <form @submit.prevent="onSubmit" class="space-y-6">
          <div class="space-y-4">
            <UInput
              v-model="form.name"
              placeholder="您的姓名 (Your Name)"
              size="lg"
              color="neutral"
              variant="outline"
              class="w-full"
              :ui="{ root: 'bg-white' }"
            />
            <UInput
              v-model="form.phone"
              placeholder="手機號碼 (Phone)"
              size="lg"
              color="neutral"
              variant="outline"
              class="w-full"
            />
          </div>

          <div class="grid grid-cols-2 gap-4">
            <div
              @click="form.attendance = 'attending'"
              class="cursor-pointer border-2 rounded-xl p-4 text-center transition-all duration-300"
              :class="
                form.attendance === 'attending'
                  ? 'border-stone-800 bg-stone-800 text-white'
                  : 'border-stone-200 text-stone-400 hover:border-stone-400'
              "
            >
              <div class="text-xl mb-1">🎉</div>
              <div class="text-sm font-bold">準時出席</div>
            </div>

            <div
              @click="form.attendance = 'declined'"
              class="cursor-pointer border-2 rounded-xl p-4 text-center transition-all duration-300"
              :class="
                form.attendance === 'declined'
                  ? 'border-stone-500 bg-stone-500 text-white'
                  : 'border-stone-200 text-stone-400 hover:border-stone-400'
              "
            >
              <div class="text-xl mb-1">🙏</div>
              <div class="text-sm font-bold">無法出席</div>
            </div>
          </div>

          <div
            v-if="form.attendance === 'attending'"
            class="space-y-6 animate-fade-in-up"
          >
            <div>
              <label
                class="block text-xs font-bold text-stone-400 uppercase tracking-widest mb-2"
                >飲食習慣 (Dietary)</label
              >
              <USelectMenu
                v-model="form.diet"
                value-key="value"
                label-key="label"
                :items="dietOptions"
                size="lg"
                color="neutral"
                variant="outline"
                :ui="{ content: 'z-[110]' }"
              />
            </div>

            <div>
              <label
                class="block text-xs font-bold text-stone-400 uppercase tracking-widest mb-2"
                >攜伴人數 (+Guest)</label
              >
              <div
                class="flex items-center justify-between border border-stone-200 rounded-lg p-2 bg-stone-50"
              >
                <UButton
                  icon="i-heroicons-minus"
                  color="neutral"
                  variant="ghost"
                  @click="form.guests > 0 ? form.guests-- : null"
                  :disabled="form.guests === 0"
                />
                <span class="font-serif text-xl w-10 text-center">{{
                  form.guests
                }}</span>
                <UButton
                  icon="i-heroicons-plus"
                  color="neutral"
                  variant="ghost"
                  @click="form.guests++"
                />
              </div>
              <p
                class="text-xs text-stone-400 mt-2 text-center"
                v-if="form.guests > 0"
              >
                共 {{ 1 + form.guests }} 位出席
              </p>
            </div>
          </div>

          <UButton
            type="submit"
            block
            size="xl"
            color="neutral"
            :loading="isSubmitting"
            class="rounded-full font-bold tracking-widest"
          >
            {{ isSubmitting ? 'SENDING...' : 'SEND RESPONSE' }}
          </UButton>
        </form>
      </div>
    </template>
  </UModal>
</template>
