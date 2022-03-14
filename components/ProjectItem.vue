<script setup>
defineProps({
  item: Object,
})

</script>

<template>
    <li class="project-item mb-2">
        <span class="project-name">
            <a :href="item.links[0]" target="_blank">{{ item.title }}</a>
        </span>&nbsp;&nbsp;
        <span class="mb-6 project-description text-gray-500 text-sm">{{ item.description }}</span>
    </li>
</template>

<style lang="postcss" scoped>

.project-item {
    transition: opacity 0.3s linear 2s;
}
.project-item .project-description {
    display:none;
}

.project-item:hover {
    cursor:pointer;
    @apply p-4;
}

.project-item:hover .project-description {
    display: inline;
}

.project-item:hover .project-name {
    font-weight: bold;
}
</style>