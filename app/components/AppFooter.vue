<script setup lang="ts">
import SocialMedia from "./SocialMedia.vue";
const year = new Date().getFullYear();
</script>

<template>
  <footer class="bg-moss-900 text-sand-100">
    <div
      class="mx-auto grid max-w-6xl gap-12 px-5 py-16 md:grid-cols-2 md:px-8 lg:grid-cols-[1.4fr_1fr_1fr_1.2fr]"
    >
      <!-- Brand -->
      <div>
        <div class="flex items-center gap-2.5 text-sand-50">
          <span class="flex flex-col leading-none">
            <span class="font-display text-xl font-semibold tracking-tight"
              >My App</span
            >
          </span>
        </div>
        <div class="mt-6 flex items-center gap-3">
          <SocialMedia />
        </div>
      </div>
    </div>

    <div class="border-t border-sand-100/10">
      <div
        class="mx-auto flex max-w-6xl flex-col items-center gap-2 px-5 py-6 text-center font-tag text-[0.7rem] uppercase tracking-wider text-moss-100/45 sm:flex-row sm:justify-between sm:text-left md:px-8"
      >
        <p>© {{ year }} My App · Musterstadt</p>
      </div>
    </div>
  </footer>
</template>
