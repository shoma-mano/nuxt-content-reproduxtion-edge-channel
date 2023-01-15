<script setup lang="ts">
const { data: cityInfo } = await useAsyncData('city',() => queryContent('city').where({id:1}).findOne());
const { data: stateInfo } = await useAsyncData('state',() => queryContent('state').where({id:1}).findOne());
</script>

<template>
  <main>
    <p>
      data fetched by queryContent('city').where({id:1}).findOne()
    </p>
    <p>
      name:{{cityInfo.name}} id:{{cityInfo.id}}
    </p>
    <p>
      data fetched by queryContent('state').where({id:1}).findOne()
    </p>
    <p>
      name:{{stateInfo.name}} id:{{stateInfo.id}}
    </p>
  </main>
</template>
