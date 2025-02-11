<template>
    <div class="w-1/2 h-1/2 bg-linear-{{sect.angle}} from-{{sect.initColor}} to-{{sect.finalColor}} border-sky-100 border-t-[{{sect.top}}] border-l-[{{sect.left}}] border-b-[{{sect.bottom}}] border-r-[{{sect.right}}] rounded-br-[100%]"></div>
</template>

<script setup>
defineProps({
    sect: Object
})
</script>

<style lang="css" scoped>

</style>