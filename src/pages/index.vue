<script setup lang="ts">
import { CashOutline as CashIcon } from '@vicons/ionicons5'

defineOptions({
  name: 'IndexPage',
})

const name = $ref('')

const router = useRouter()
function go() {
  if (name)
    router.push(`/hi/${encodeURIComponent(name)}`)
}
</script>

<template>
  <div>
    <div i-carbon-campsite inline-block text-4xl />
    <p>
      <a rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank">
        Vitesse Lite
      </a>
    </p>
    <p>
      <em text-sm op75>Opinionated Vite Starter Template</em>
    </p>

    <div py-4 />

    <TheInput
      v-model="name"
      placeholder="What's your name?"
      autocomplete="false"
      @keydown.enter="go"
    />

    <div>
      <button
        class="m-3 text-sm btn"
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
            <n-icon><CashIcon /></n-icon>
          </template>
        </n-button>
        <n-button strong secondary circle type="primary">
          <template #icon>
            <n-icon><CashIcon /></n-icon>
          </template>
        </n-button>
        <n-button strong secondary circle type="info">
          <template #icon>
            <n-icon><CashIcon /></n-icon>
          </template>
        </n-button>
        <n-button strong secondary circle type="success">
          <template #icon>
            <n-icon><CashIcon /></n-icon>
          </template>
        </n-button>
        <n-button strong secondary circle type="warning">
          <template #icon>
            <n-icon><CashIcon /></n-icon>
          </template>
        </n-button>
        <n-button strong secondary circle type="error">
          <template #icon>
            <n-icon><CashIcon /></n-icon>
          </template>
        </n-button>
      </n-space>
    </div>
  </div>
</template>
