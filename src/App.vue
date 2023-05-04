<script lang="ts" setup>
import { NConfigProvider, dateItIT, itIT } from 'naive-ui'
</script>

<template>
  <NConfigProvider :locale="itIT" :date-locale="dateItIT">
    <n-notification-provider>
      <n-loading-bar-provider>
        <n-message-provider>
          <suspense>
            <n-dialog-provider>
              <main font-sans p="x-4 y-10" text="center gray-700 dark:gray-200">
                <router-view />
                <TheFooter />
              </main>
            </n-dialog-provider>
          </suspense>
        </n-message-provider>
      </n-loading-bar-provider>
    </n-notification-provider>
  </NConfigProvider>
</template>
