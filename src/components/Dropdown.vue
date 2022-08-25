<template>

    <div class="menu-item" @click="isOpen = !isOpen">
        <a href="#">
            {{ title }}
        </a>

        <transition name="melkor" appear>
            <div class="sub-menu" v-if="isOpen">
                <div v-for="(item, i) in items" :key="i" class="menu-item">
                    <a :href="item.link">{{ item.title }}</a>
                </div>
            </div>
        </transition>
    </div>
</template>


<script>
export default {
    name: 'dropdownVue',
    props: ['title', 'items'],
    data() {
        return {
            isOpen: false
        }
    }
}
</script>


<style>
nav .menu-item .sub-menu {
    position: absolute;
    background-color: #222;
    top: calc(100% + 18px);
    transform: translateX(-50%);
    left: 50%;
    width: max-content;
    border-radius: 0px 0px 16px 16px;
}

.melkor-enter-active,
.melkor-leave-active {
    transition: all .5s ease-out;

}

.melkor-enter,
.melkor-leave-to {
    opacity: 0;
}
</style>