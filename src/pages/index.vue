<script setup lang="ts">
  import { CashOutline as CashIcon } from '@vicons/ionicons5'
  import { defineComponent } from 'vue'

const name = $ref('')

const router = useRouter()
const go = () => {
  if (name)
    router.push(`/hi/${encodeURIComponent(name)}`)
}

  </script>

<template>
  <div>
    <div i-carbon-campsite text-4xl inline-block />
    <p>
      <a rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank">
        Vitesse Lite
      </a>
    </p>
    <p>
      <em text-sm op75>Opinionated Vite Starter Template</em>
    </p>

    <div py-4 />

    <input
      id="input"
      v-model="name"
      placeholder="What's your name?"
      type="text"
      autocomplete="false"
      p="x-4 y-2"
      w="250px"
      text="center"
      bg="transparent"
      border="~ rounded gray-200 dark:gray-700"
      outline="none active:none"
      @keydown.enter="go"
    >

    <div>
      <button
        class="mt-3 text-sm btn"
        :disabled="!name"
        @click="go"
      >
        Go
      </button>
    </div>

    <div class="mt-10">
      <n-space justify="center">
          <n-button>Default</n-button>
          <n-button type="tertiary">
            Tertiary
          </n-button>
          <n-button type="primary">
            Primary
          </n-button>
          <n-button type="info">
            Info
          </n-button>
          <n-button type="success">
            Success
          </n-button>
          <n-button type="warning">
            Warning
          </n-button>
          <n-button type="error">
            Error
          </n-button>
      </n-space>

      </div>

      <div class="mt-10">
      <n-space justify="center">
      <n-button strong secondary>
        Default
      </n-button>
      <n-button strong secondary type="tertiary">
        Tertiary
      </n-button>
      <n-button strong secondary type="primary">
        Primary
      </n-button>
      <n-button strong secondary type="info">
        Info
      </n-button>
      <n-button strong secondary type="success">
        Success
      </n-button>
      <n-button strong secondary type="warning">
        Warning
      </n-button>
      <n-button strong secondary type="error">
        Error
      </n-button>
      <n-button strong secondary round>
        Default
      </n-button>
      <n-button strong secondary round type="primary">
        Primary
      </n-button>
      <n-button strong secondary round type="info">
        Info
      </n-button>
      <n-button strong secondary round type="success">
        Success
      </n-button>
      <n-button strong secondary round type="warning">
        Warning
      </n-button>
      <n-button strong secondary round type="error">
        Error
      </n-button>
      <n-button strong secondary circle>
        <template #icon>
          <n-icon><cash-icon /></n-icon>
        </template>
      </n-button>
      <n-button strong secondary circle type="primary">
        <template #icon>
          <n-icon><cash-icon /></n-icon>
        </template>
      </n-button>
      <n-button strong secondary circle type="info">
        <template #icon>
          <n-icon><cash-icon /></n-icon>
        </template>
      </n-button>
      <n-button strong secondary circle type="success">
        <template #icon>
          <n-icon><cash-icon /></n-icon>
        </template>
      </n-button>
      <n-button strong secondary circle type="warning">
        <template #icon>
          <n-icon><cash-icon /></n-icon>
        </template>
      </n-button>
      <n-button strong secondary circle type="error">
        <template #icon>
          <n-icon><cash-icon /></n-icon>
        </template>
      </n-button>
      </n-space>
    </div>

  </div>
</template>
