<script setup lang="ts">
const { data: info } = await useAsyncData('city',() => queryContent('city').where({id:1}).findOne());


const generatedAt = useState(() => new Date().toISOString())
</script>

<template>
  <main>
    <p>
      data fetched by queryContent('city').where({id:1}).findOne()
    </p>
    <p>
      {{info}}
    </p>
  </main>
</template>
