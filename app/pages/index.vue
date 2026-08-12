<script setup lang="ts">
useHead({
  title: "Bei Momo – Hundesalon in Musterstadt",
  meta: [
    {
      name: "description",
      content:
        "Hundesalon Bei Momo in Musterstadt: Fellpflege ohne Zeitdruck, Handarbeit für Halsbänder und Leinen sowie das Momo-Programm für deinen Vierbeiner.",
    },
  ],
});

const highlights = [
  {
    icon: "clock",
    title: "Zeit statt Taktung",
    body: "Ein Hund pro Termin. Kein Wartekäfig, keine Hektik – wir arbeiten im Tempo deines Vierbeiners.",
  },
  {
    icon: "check",
    title: "Ehrliche Preise",
    body: "Abgerechnet wird nach Aufwand, nicht nach Rasse. Was es kostet, sagen wir vorher – nicht danach.",
  },
  {
    icon: "star",
    title: "Sanfte Produkte",
    body: "Shampoos und Pflegemittel ohne Silikone und Parabene, abgestimmt auf Fell und Haut.",
  },
];

const services = [
  {
    title: "Komplettpflege",
    body: "Der große Termin: dein Hund kommt struppig rein und geht als bessere Version seiner selbst wieder raus. Wir nehmen uns zwei Stunden dafür.",
    price: "ab € 65,–",
    priceNote: "je nach Größe & Fell",
    label: "Foto: Hund beim Fellschnitt",
  },
  {
    title: "Wäsche & Bürsten",
    body: "Für alle, die es nach dem Waldspaziergang eilig haben. Nach 45 Minuten riecht dein Sofa wieder wie ein Sofa.",
    price: "ab € 35,–",
    priceNote: "ca. 45 Minuten",
    label: "Foto: Hund in der Badewanne",
  },
  {
    title: "Handarbeit & Zubehör",
    body: "Halsbänder und Leinen, die wir nebenan selbst flechten. Farbe aussuchen, Maß nehmen, in einer Woche ist es fertig.",
    price: "ab € 24,–",
    priceNote: "Einzelstücke",
    label: "Foto: Halsbänder aus Paracord",
  },
  {
    title: "Momo-Programm & Balance",
    body: "Für ältere Hunde, steife Gelenke und alle, denen der Winter in den Knochen sitzt. Ruhig, warm, ohne Leistungsdruck.",
    price: "ab € 45,–",
    priceNote: "pro Einheit",
    label: "Foto: Hund bei Momo-Programm",
  },
];

const team = [
  {
    name: "Muster Max",
    role: "Inhaber & Groomer",
    body: "Gelernter Hundefriseur, seit zwölf Jahren im Beruf. Spezialist für Handstripping und schwierige Kandidaten.",
    label: "Foto: Muster Max",
  },
  {
    name: "Beispiel Anna",
    role: "Groomerin & Momo-Programm",
    body: "Kümmert sich um Pflege und das Momo-Programm. Hat für jeden nervösen Hund einen langen Atem.",
    label: "Foto: Beispiel Anna",
  },
];

const reviews = [
  {
    name: "Bruno",
    breed: "Berner Sennenhund, 6 Jahre",
    paws: 5,
    quote:
      "War skeptisch. Bin dann eingeschlafen. Habe verschlafen, dass ich fertig war. Fünf von fünf, würde wieder pennen.",
    label: "Foto: Bruno",
  },
  {
    name: "Kleopatra",
    breed: "Pudel, 3 Jahre",
    paws: 5,
    quote:
      "Endlich jemand, der versteht, dass ich links anders aussehen will als rechts. Frauchen versteht das bis heute nicht.",
    label: "Foto: Kleopatra",
  },
  {
    name: "Rocky",
    breed: "Jack Russell, 2 Jahre",
    paws: 4,
    quote:
      "Ein Punkt Abzug, weil das Wasser nass war. Ansonsten: viele Streicheleinheiten, gutes Personal, komme wieder.",
    label: "Foto: Rocky",
  },
  {
    name: "Frau Schneider",
    breed: "Dackel, 9 Jahre",
    paws: 5,
    quote:
      "In meinem Alter geht man nicht mehr überall hin. Hier gehe ich hin. Die haben eine warme Decke und Geduld.",
    label: "Foto: Frau Schneider",
  },
];
</script>

<template>
  <div>
    <!-- Hero -->
    <section class="relative overflow-hidden bg-moss-900">
      <div
        class="mx-auto grid max-w-6xl gap-12 px-5 py-20 md:grid-cols-[1.1fr_1fr] md:items-center md:px-8 md:py-32"
      >
        <div>
          <p class="eyebrow-tag text-gold-400">Hundesalon · Musterstadt</p>
          <h1
            class="mt-4 font-display text-4xl font-semibold leading-[1.05] text-sand-50 sm:text-5xl lg:text-6xl"
          >
            Fellpflege, nach der dein<br class="hidden sm:block" />
            Hund gern wiederkommt.
          </h1>
          <p class="mt-6 max-w-md text-lg leading-relaxed text-moss-100/85">
            Fellpflege ohne Zeitdruck, in einem ruhigen Salon mitten in
            Musterstadt. Ein Hund pro Termin – und so viel Zeit, wie er braucht.
          </p>

          <div class="mt-9 flex flex-wrap gap-3">
            <NuxtLink
              to="/kontakt"
              class="inline-flex items-center gap-2 rounded-full bg-clay-500 px-6 py-3.5 text-sm font-semibold text-sand-50 shadow-tag transition-colors duration-200 hover:bg-clay-600"
            >
              Termin anfragen
              <FontAwesomeIcon :icon="['fas', 'envelope']" />
            </NuxtLink>
            <NuxtLink
              to="/leistungen"
              class="rounded-full border border-sand-100/30 px-6 py-3.5 text-sm font-semibold text-sand-50 transition-colors hover:bg-sand-100/10"
            >
              Preise ansehen
            </NuxtLink>
          </div>

          <p class="mt-8 flex items-center gap-2 text-sm text-moss-100/70">
            <FontAwesomeIcon :icon="['fas', 'phone']" class="text-gold-400" />
            Lieber kurz anrufen? 01234 / 56 78 90
          </p>
        </div>

        <ImgPlaceholder
          label="Foto: Hund im Bei Momo Salon"
          ratio="aspect-[4/5]"
          tone="clay"
        />
      </div>
    </section>

    <!-- Highlights -->
    <section class="mx-auto max-w-6xl px-5 py-16 md:px-8 md:py-20">
      <div class="grid gap-6 sm:grid-cols-3">
        <div
          v-for="item in highlights"
          :key="item.title"
          class="tag-card p-6 pl-8"
        >
          <FontAwesomeIcon
            :icon="['fas', item.icon]"
            class="text-2xl text-clay-600"
          />
          <h2 class="mt-4 font-display text-lg font-semibold text-moss-900">
            {{ item.title }}
          </h2>
          <p class="mt-2 text-sm leading-relaxed text-ink-700">
            {{ item.body }}
          </p>
        </div>
      </div>
    </section>

    <!-- Leistungen -->
    <section class="bg-sand-100">
      <div class="mx-auto max-w-6xl px-5 py-16 md:px-8 md:py-20">
        <p class="eyebrow-tag text-clay-600">Leistungen</p>
        <h2
          class="mt-3 max-w-2xl font-display text-3xl font-semibold text-moss-900 sm:text-4xl"
        >
          Vom kurzen Bad bis zur kompletten Verwandlung.
        </h2>
        <p class="mt-4 max-w-xl leading-relaxed text-ink-700">
          Alle Preise sind Richtwerte – was dein Hund wirklich braucht,
          besprechen wir vorher in Ruhe.
        </p>

        <div class="mt-12 grid gap-8 sm:grid-cols-2 lg:grid-cols-4">
          <article
            v-for="service in services"
            :key="service.title"
            class="tag-card flex flex-col p-6 pl-8"
          >
            <ImgPlaceholder
              :label="service.label"
              ratio="aspect-[4/3]"
              tone="sand"
            />
            <h3 class="mt-5 font-display text-xl font-semibold text-moss-900">
              {{ service.title }}
            </h3>
            <p class="mt-2 flex-1 text-sm leading-relaxed text-ink-700">
              {{ service.body }}
            </p>
            <p class="mt-4 border-t border-sand-200 pt-4 font-tag text-sm">
              <span class="font-semibold text-clay-600">{{
                service.price
              }}</span>
              <span class="ml-2 text-ink-700/60">{{ service.priceNote }}</span>
            </p>
          </article>
        </div>

        <NuxtLink
          to="/leistungen"
          class="mt-10 inline-flex items-center gap-2 font-semibold text-clay-600 underline underline-offset-4"
        >
          Komplette Preisliste ansehen
          <FontAwesomeIcon :icon="['fas', 'arrow-right']" class="text-xs" />
        </NuxtLink>
      </div>
    </section>

    <!-- Hundebewertungen -->
    <section class="mx-auto max-w-6xl px-5 py-16 md:px-8 md:py-20">
      <p class="eyebrow-tag text-clay-600">Bewertungen</p>
      <h2
        class="mt-3 max-w-2xl font-display text-3xl font-semibold text-moss-900 sm:text-4xl"
      >
        Was unsere Kunden sagen.
      </h2>
      <p class="mt-4 max-w-xl leading-relaxed text-ink-700">
        Nicht die mit dem Geldbeutel – die mit der Rute. Frei übersetzt aus dem
        Hündischen.
      </p>

      <div class="mt-12 grid gap-6 sm:grid-cols-2">
        <figure
          v-for="review in reviews"
          :key="review.name"
          class="tag-card flex flex-col p-6 pl-8"
        >
          <div class="flex items-center gap-4">
            <div class="h-14 w-14 shrink-0 overflow-hidden rounded-full">
              <ImgPlaceholder
                :label="review.label"
                ratio="aspect-square"
                tone="moss"
              />
            </div>

            <figcaption class="min-w-0">
              <p class="font-display text-lg font-semibold text-moss-900">
                {{ review.name }}
              </p>
              <p class="text-xs text-ink-700/70">{{ review.breed }}</p>
            </figcaption>
          </div>

          <div
            class="mt-4 flex items-center gap-1"
            :aria-label="`${review.paws} von 5 Pfoten`"
          >
            <PawMark
              v-for="n in 5"
              :key="n"
              class="h-4 w-4"
              :class="n <= review.paws ? 'text-clay-500' : 'text-sand-200'"
            />
          </div>

          <blockquote
            class="mt-4 flex-1 text-[0.95rem] leading-relaxed text-ink-700"
          >
            „{{ review.quote }}"
          </blockquote>
        </figure>
      </div>

      <p class="mt-8 text-center text-xs text-ink-700/50">
        Alle Bewertungen von echten Hunden. Übersetzungsfehler vorbehalten.
      </p>
    </section>

    <!-- Aktuelles -->
    <section class="bg-sand-100">
      <div class="mx-auto max-w-6xl px-5 py-16 md:px-8 md:py-20">
        <p class="eyebrow-tag text-clay-600">Aktuelles</p>
        <h2
          class="mt-3 max-w-2xl font-display text-3xl font-semibold text-moss-900 sm:text-4xl"
        >
          Was es bei uns gerade Neues gibt.
        </h2>
        <p class="mt-4 max-w-xl leading-relaxed text-ink-700">
          Terminlage, Urlaubszeiten und alles, was du vor deinem Besuch wissen
          solltest.
        </p>

        <NewsCard />
      </div>
    </section>

    <!-- Team -->
    <section class="mx-auto max-w-6xl px-5 py-16 md:px-8 md:py-20">
      <div class="grid gap-x-12 gap-y-8 lg:grid-cols-[1fr_1.2fr] lg:gap-y-6">
        <!-- Intro -->
        <div class="lg:col-start-1 lg:row-start-1 lg:self-end">
          <p class="eyebrow-tag text-clay-600">Das Team</p>
          <h2
            class="mt-3 font-display text-3xl font-semibold text-moss-900 sm:text-4xl"
          >
            Zwei Paar Hände, die wissen, was sie tun.
          </h2>
          <p class="mt-4 leading-relaxed text-ink-700">
            Wir sind ein kleiner Salon und wollen das auch bleiben. So kennen
            wir jeden Hund beim Namen – und merken uns, wer die Föhnstufe lieber
            leise mag.
          </p>
        </div>

        <!-- Members -->
        <div
          class="grid gap-6 sm:grid-cols-2 lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:self-center"
        >
          <article
            v-for="member in team"
            :key="member.name"
            class="tag-card p-6 pl-8"
          >
            <ImgPlaceholder
              :label="member.label"
              ratio="aspect-square"
              tone="moss"
            />
            <h3 class="mt-5 font-display text-lg font-semibold text-moss-900">
              {{ member.name }}
            </h3>
            <p class="eyebrow-tag mt-1 text-clay-600">{{ member.role }}</p>
            <p class="mt-3 text-sm leading-relaxed text-ink-700">
              {{ member.body }}
            </p>
          </article>
        </div>

        <!-- CTA -->
        <div
          class="text-center lg:col-start-1 lg:row-start-2 lg:self-start lg:text-left"
        >
          <NuxtLink
            to="/ueber-uns"
            class="inline-flex items-center gap-2 rounded-full bg-moss-800 px-6 py-3.5 text-sm font-semibold text-sand-50 shadow-tag transition-colors duration-200 hover:bg-moss-700"
          >
            Mehr über uns
            <FontAwesomeIcon :icon="['fas', 'arrow-right']" />
          </NuxtLink>
        </div>
      </div>
    </section>

    <!-- CTA -->
    <section class="bg-moss-900">
      <div class="mx-auto max-w-3xl px-5 py-16 text-center md:px-8 md:py-20">
        <h2
          class="font-display text-3xl font-semibold text-sand-50 sm:text-4xl"
        >
          Noch keinen Termin?
        </h2>
        <p class="mx-auto mt-4 max-w-md leading-relaxed text-moss-100/85">
          Schreib uns kurz, worum es geht – wir melden uns meist noch am selben
          Tag zurück.
        </p>
        <NuxtLink
          to="/kontakt"
          class="mt-8 inline-flex items-center gap-2 rounded-full bg-clay-500 px-6 py-3.5 text-sm font-semibold text-sand-50 shadow-tag transition-colors duration-200 hover:bg-clay-600"
        >
          <FontAwesomeIcon :icon="['fas', 'envelope']" />
          Jetzt anfragen
        </NuxtLink>
      </div>
    </section>
  </div>
</template>
