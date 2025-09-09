<script setup lang="ts">
const columns = [{
  label: 'Servicios',
  children: [{
    label: 'Networking'
  }, {
    label: 'Seguridad Perimetral'
  }, {
    label: 'Virtualización'
  }, {
    label: 'Infraestructura'
  }, {
    label: 'Cloud Computing'
  }]
}, {
  label: 'Empresa',
  children: [{
    label: 'Sobre Nosotros'
  }, {
    label: 'Consultoría'
  }, {
    label: 'Casos de Éxito'
  }, {
    label: 'Blog Técnico'
  }]
}, {
  label: 'Contacto',
  children: [{
    label: 'Teléfono: +34 657 99 20 52'
  }, {
    label: 'Email: info@it-suru.es'
  }, {
    label: 'C/ Sant Manuel, 5'
  }, {
    label: 'Barcelona, 08031'
  }]
}]

const toast = useToast()

const email = ref('')
const loading = ref(false)

function onSubmit() {
  loading.value = true

  toast.add({
    title: 'Subscribed!',
    description: 'You\'ve been subscribed to our newsletter.'
  })
}
</script>

<template>
  <USeparator
    icon="i-simple-icons-nuxtdotjs"
    class="h-px"
  />

  <UFooter :ui="{ top: 'border-b border-default' }">
    <template #top>
      <UContainer>
        <UFooterColumns :columns="columns">
          <template #right>
            <form @submit.prevent="onSubmit">
              <UFormField
                name="email"
                label="Suscríbete a nuestro boletín"
                size="lg"
              >
                <UInput
                  v-model="email"
                  type="email"
                  class="w-full"
                  placeholder="Introduce tu email"
                >
                  <template #trailing>
                    <UButton
                      type="submit"
                      size="xs"
                      label="Suscribir"
                    />
                  </template>
                </UInput>
              </UFormField>
            </form>
          </template>
        </UFooterColumns>
      </UContainer>
    </template>

    <template #left>
      <p class="text-sm text-muted">
        IT Suru - Consultoría IT Especializada • © {{ new Date().getFullYear() }}
      </p>
    </template>

    <template #right>
      <UButton
        to="https://www.linkedin.com/company/itsuru"
        target="_blank"
        icon="i-simple-icons-linkedin"
        aria-label="IT Suru en LinkedIn"
        color="neutral"
        variant="ghost"
      />
      <UButton
        to="https://twitter.com/itsuru"
        target="_blank"
        icon="i-simple-icons-x"
        aria-label="IT Suru en X"
        color="neutral"
        variant="ghost"
      />
      <UButton
        to="mailto:info@it-suru.es"
        icon="i-lucide-mail"
        aria-label="Contactar IT Suru"
        color="neutral"
        variant="ghost"
      />
    </template>
  </UFooter>
</template>
