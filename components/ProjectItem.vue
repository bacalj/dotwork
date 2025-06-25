<script setup>
defineProps({
  item: Object,
})

</script>

<template>
    <li class="project-item mb-2">
        <span class="project-name">
            <!-- <span v-if="item.star"> ⭐ </span><a :href="item.links[0]" target="_blank">{{ item.title }}</a> -->
        </span>&nbsp;&nbsp;<br>
        <span class="mb-6 project-description text-gray-500 text-sm">{{ item.description }}</span>
    </li>
</template>
