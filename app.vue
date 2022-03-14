<script setup>

  const query = groq`*[_type == "project"]`
  const { data } = await useSanityQuery(query)

  
  console.log(data.value)

</script>


<template>
  <div class="p-8 bg-gray-50">
    <h1 class="text-lg font-bold text-gray-800 pb-12">joebacal.work</h1>

      <ul class="projects">
        <project-item class="text-gray-800" v-for="(d, i) in data" :key="i" :item="d"></project-item>
      </ul>

  </div>
</template>
