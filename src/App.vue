<script lang="ts" setup>
  import { dateItIT, itIT, NConfigProvider } from 'naive-ui'
</script>

<template>
  <n-config-provider :locale="itIT" :date-locale="dateItIT">
    <n-notification-provider>
      <n-loading-bar-provider>
        <n-message-provider>
          <suspense>
            <n-dialog-provider>
              <main font-sans p="x-4 y-10" text="center gray-700 dark:gray-200">
                <router-view />
                <Footer />
              </main>
            </n-dialog-provider>
          </suspense>
        </n-message-provider>
      </n-loading-bar-provider>
    </n-notification-provider>
  </n-config-provider>
</template>
