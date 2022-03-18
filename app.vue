<script setup>

  const query = groq`*[_type == "project" && !(_id in path('drafts.**'))]| order(title asc)`
  const { data } = await useSanityQuery(query)

  
  console.log(data.value)

</script>


<template>
  <div class="p-6 bg-gray-50">
    <h1 class="text-lg font-bold text-gray-800 pb-6">joebacal.work</h1>

      <hr class="mb-3">

      <div class="pb-6 text-gray-600">
        Web dev projects have a ⭐.  <br>The others are either utilities or static materials.
        <br>Stay tuned as there are more items to dig up...
        <br> <a href="https://github.com/bacalj">GitHub</a> | <a href="https://twitter.com/joe_bacal">Twitter</a>
      </div>

      <hr class="mb-3">

      <ul class="projects">
        <project-item class="text-gray-800" v-for="(d, i) in data" :key="i" :item="d"></project-item>
      </ul>

  </div>
</template>

<style lang="postcss" scoped>
a:hover {
  font-weight: bold;
}
</style>