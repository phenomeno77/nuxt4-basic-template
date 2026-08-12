<template>
  <div class="flex min-h-screen flex-col bg-sand-50">
    <AppNavbar />
    <main class="flex-1">
      <slot />
    </main>
    <AppFooter />
  </div>
</template>
