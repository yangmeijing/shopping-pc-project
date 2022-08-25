<template>
    <AppNavbar />
    <AppHeader />
    <main class="app-body">
        <RouterView />
    </main>
    <AppFooter />
</template>
<script setup>
import AppNavbar from '@/components/app-navbar.vue'
import AppHeader from '@/components/app-header.vue'
import AppFooter from '@/components/app-footer.vue'
import { useStore } from 'vuex';

// 获取分类数据
const store = useStore()
store.dispatch('category/getList')
</script>
<style>
.app-body{
    min-height: 600px;
}
</style>
