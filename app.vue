<script setup>

  const query = groq`*[_type == "project"]`
  const { data, refresh } = useSanityQuery(query)  

  console.log(data)
</script>


<template>
  <div>
    hello
  </div>
</template>
