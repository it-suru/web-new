<script setup lang="ts">
const nuxtApp = useNuxtApp()
const { activeHeadings, updateHeadings } = useScrollspy()

const items = computed(() => [{
  label: 'Servicios',
  to: '#features',
  active: activeHeadings.value.includes('features') && !activeHeadings.value.includes('pricing')
}, {
  label: 'Consultoría',
  to: '#pricing',
  active: activeHeadings.value.includes('pricing')
}, {
  label: 'Testimonios',
  to: '#testimonials',
  active: activeHeadings.value.includes('testimonials') && !activeHeadings.value.includes('pricing')
}])

nuxtApp.hooks.hookOnce('page:finish', () => {
  updateHeadings([
    document.querySelector('#features'),
    document.querySelector('#pricing'),
    document.querySelector('#testimonials')
  ].filter(Boolean) as Element[])
})
</script>

<template>
  <UHeader>
    <template #left>
      <NuxtLink to="/">
        <AppLogo class="w-auto h-6 shrink-0" />
      </NuxtLink>
    </template>

    <template #right>
      <UNavigationMenu
        :items="items"
        variant="link"
        class="hidden lg:block"
      />

      <UButton
        label="Consulta Gratuita"
        variant="subtle"
        class="hidden lg:block"
        to="#contacto"
      />

      <UColorModeButton />
    </template>

    <template #body>
      <UNavigationMenu
        :items="items"
        orientation="vertical"
        class="-mx-2.5"
      />
      <UButton
        class="mt-4"
        label="Consulta Gratuita"
        variant="subtle"
        block
        to="#contacto"
      />
    </template>
  </UHeader>
</template>
