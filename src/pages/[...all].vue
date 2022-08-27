<script setup>
import {useAppStore} from "../store";

const router = useRouter();
const appStore = useAppStore()
const onBack = ()=> {
  appStore.$patch({
    token: '111'
  })
  router.push('/')
}
</script>

<template>
  <main p="x4 y10" text="center teal-700 dark:gray-200" bg-surface h-screen>
    <div text-4xl>
      <div i-carbon-warning inline-block />
    </div>
    <router-view />
    <div>
      <button btn text-sm m="3 t8" @click="onBack">返回</button>
    </div>
  </main>
</template>
