<script setup lang="ts">
const open = ref(false);

const links = navLinks;

const phone = "+49123456789";
const phoneLabel = "01234 / 56 78 90";

const route = useRoute();
watch(
  () => route.fullPath,
  () => {
    open.value = false;
  },
);

// Lock body scroll while the mobile menu is open
watch(open, (isOpen) => {
  if (import.meta.client) {
    document.body.style.overflow = isOpen ? "hidden" : "";
  }
});

onUnmounted(() => {
  if (import.meta.client) document.body.style.overflow = "";
});
</script>

<template>
  <header
    class="sticky top-0 z-50 border-b border-sand-200 bg-sand-50/85 backdrop-blur-md"
  >
    <div
      class="mx-auto flex max-w-6xl items-center justify-between gap-4 px-5 py-3.5 md:px-8"
    >
      <!-- Brand -->
      <NuxtLink
        to="/"
        class="flex items-center gap-2.5 text-moss-900"
        aria-label="My App – zur Startseite"
      >
        <PawMark class="h-8 w-8 shrink-0 text-clay-600" />
        <span class="flex flex-col leading-none">
          <span class="font-display text-xl font-semibold tracking-tight"
            >My App</span
          >
          <span class="eyebrow-tag mt-0.5 text-ink-700/60"></span>
        </span>
      </NuxtLink>

      <!-- Desktop nav -->
      <nav class="hidden items-center gap-1 lg:flex">
        <NuxtLink
          v-for="link in links"
          :key="link.to"
          :to="link.to"
          class="relative rounded-full px-3.5 py-2 text-[0.95rem] text-ink-700 transition-colors hover:text-moss-900"
          active-class="!text-moss-900 font-semibold after:absolute after:inset-x-3.5 after:-bottom-0.5 after:h-0.5 after:rounded-full after:bg-clay-500"
        >
          {{ link.label }}
        </NuxtLink>
      </nav>

      <!-- Desktop CTA -->
      <a
        :href="`tel:${phone}`"
        class="hidden items-center gap-2 rounded-full bg-moss-800 px-5 py-2.5 text-sm font-semibold text-sand-50 shadow-tag transition-transform hover:-translate-y-0.5 lg:inline-flex"
      >
        <FontAwesomeIcon :icon="['fas', 'phone']" />
        {{ phoneLabel }}
      </a>

      <!-- Mobile actions -->
      <div class="flex items-center gap-2 lg:hidden">
        <a
          :href="`tel:${phone}`"
          class="flex h-11 w-11 items-center justify-center rounded-full bg-moss-800 text-sand-50"
          aria-label="Anrufen"
        >
          <FontAwesomeIcon :icon="['fas', 'phone']" />
        </a>

        <button
          type="button"
          class="flex h-11 w-11 items-center justify-center rounded-full border border-sand-200 bg-sand-100 text-moss-900"
          :aria-expanded="open"
          aria-controls="mobile-menu"
          :aria-label="open ? 'Menü schließen' : 'Menü öffnen'"
          @click="open = !open"
        >
          <span class="relative flex h-4 w-5 flex-col justify-between">
            <span
              class="h-0.5 w-full rounded-full bg-current transition-transform duration-200"
              :class="open ? 'translate-y-[7px] rotate-45' : ''"
            />
            <span
              class="h-0.5 w-full rounded-full bg-current transition-opacity duration-200"
              :class="open ? 'opacity-0' : ''"
            />
            <span
              class="h-0.5 w-full rounded-full bg-current transition-transform duration-200"
              :class="open ? '-translate-y-[7px] -rotate-45' : ''"
            />
          </span>
        </button>
      </div>
    </div>

    <!-- Mobile menu -->
    <Transition
      enter-active-class="transition duration-200 ease-out"
      enter-from-class="opacity-0 -translate-y-3"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition duration-150 ease-in"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-3"
    >
      <nav
        v-if="open"
        id="mobile-menu"
        class="border-t border-sand-200 bg-sand-50 px-5 pb-6 pt-4 lg:hidden"
      >
        <NuxtLink
          v-for="link in links"
          :key="link.to"
          :to="link.to"
          class="flex items-center justify-between rounded-xl px-4 py-3.5 text-base text-ink-700 transition-colors hover:bg-moss-100/60"
          active-class="bg-moss-100 !text-moss-900 font-semibold"
        >
          {{ link.label }}
        </NuxtLink>

        <NuxtLink
          to="/kontakt"
          class="mt-4 flex items-center justify-center gap-2 rounded-full bg-clay-500 px-5 py-3.5 text-sm font-semibold text-sand-50 shadow-tag"
        >
          <FontAwesomeIcon :icon="['fas', 'envelope']" />
          Termin anfragen
        </NuxtLink>
      </nav>
    </Transition>
  </header>
</template>
