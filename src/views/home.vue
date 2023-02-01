<template>
  <div>Home</div>
  <div>
    <el-button :icon="Minus" @click="changeCounter(false)" />
    {{ counter.count }}
    <el-button :icon="Plus" @click="changeCounter(true)" />
  </div>
</template>

<script lang="ts" setup>
import { Plus, Minus } from '@element-plus/icons-vue'

import { useCounterStore } from '@/store/counter'

const counter = useCounterStore()

const changeCounter = (isAdd: boolean) => {
  if (isAdd) {
    counter.increment()
  } else {
    counter.minus()
  }
}
</script>

<style></style>
