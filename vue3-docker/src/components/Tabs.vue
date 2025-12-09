
<template>
  <div>
    <div class="tabs">
         </div>

    <div class="content">
      <div v-if="activeTab === 'tab1'">
        <h2>Data from Golang API:</h2>
        <pre>{{ jsonData }}</pre>
      </div>
      <div v-else>
        <h2>{{ activeTab }} Content</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const tabs = ['tab1', 'tab2', 'tab3', 'tab4', 'tab5']
const activeTab = ref('tab1')
const jsonData = ref('Loading...')

console.log('111111')
onMounted(async () => {
  console.log('222222')
  const res = await fetch('http://127.0.0.1:8080')
  console.log('3333333')
  jsonData.value = await res.json()
  console.log('5555555')
})
</script>

<style>
.tabs button {
  margin: 5px;
  padding: 10px;
}
</style>
