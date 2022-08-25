<template>

    <div class="menu-item">
        <a href="#">
            {{ title }}
        </a>
    </div>

</template>


<script>
export default {
    name: 'dropdownVue',
    props: ['title', 'items']
}
</script>


<style>
</style>