<script setup>

const query = groq`{ "projects": *[_type == "project"] }`

const sanity = useSanity()

const { data } = await useAsyncData('projects', () => sanity.fetch(query))

  console.log(data)
</script>


<template>
  <div>
    <pre>
         {{ data }}
    </pre>
 
  </div>
</template>
