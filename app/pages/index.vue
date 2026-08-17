<script setup lang="ts">
import SectionTitle from "~/components/ui/SectionTitle.vue";

useSeoMeta({
  titleTemplate: (title) =>
    title ? `${title} — Meine Seite` : "Meine Seite – irgendwo in Musterstadt",
  description: "Beschreibung kommt hier...",
  ogImage: "/icon-512.png",
  ogImageAlt: "Meine Seite – irgendwo in Musterstadt",
  twitterCard: "summary", // "summary" suits a square image; "summary_large_image" for the 1200×630
  twitterTitle: "Meine Seite – irgendwo in Musterstadt",
  twitterDescription: "Beschreibung kommt hier...",
  twitterImage: "/icon-512.png",
});

useHead({
  htmlAttrs: { lang: "de" },
});
</script>

<template>
  <div class="container-custom">
    Homepage
    <SectionTitle
      eyebrow="Behind the Art"
      title="How I Work"
      description="A quick look at what goes into a finished piece, from first sketch to final render."
    />
  </div>
</template>
