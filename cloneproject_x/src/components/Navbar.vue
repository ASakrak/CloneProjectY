<template>
    <nav>
        <div class="menu-item"><a href="#">Blizzard</a></div>
        <div class="menu-item"><a href="#">Warcraft</a></div>
        <div class="menu-item"><a href="#">Diablo</a></div>
        <div class="menu-item"><a href="#">Overwatch</a></div>
        <div class="menu-item"><a href="#">StarCraft</a></div>
        <Dropdown title="Test" :items="Test" />
        <div class="menu-item"><a href="#">...</a></div>
    </nav>
</template>

<script>
import Dropdown from './Dropdown.vue'



export default {
    name: "navbarVue",
    components: {
        Dropdown
    },
    data() {
        return {
            Test: [
                {
                    title: "first",
                    link: "#"
                },
                {
                    title: "second",
                    link: "#"
                },
                {
                    title: "third",
                    link: "#"
                }
            ]
        };
    },

}
</script>

<style>
nav {
    display: flex;
    align-items: center;
    justify-content: center;

}

nav .menu-item {
    color: #fff;
    padding: 10px 20px;
    position: relative;
    text-align: center;
    border-bottom: 3px solid transparent;
    display: flex;
    transition: 0.4s;

}

nav .menu-item.active,
nav .menu-item:hover {
    background-color: rgb(0, 0, 0);
    border-bottom-color: rgb(165, 165, 165);
}

nav .menu-item a {
    color: inherit;
    text-decoration: none;

}
</style>
