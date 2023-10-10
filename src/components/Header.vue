<script>

import mainMenu from '../data/mainMenu';

  export default {
    name: 'Header',
    data () {
        return {
            mainMenu
        }
    }
};
</script>

<template>
    <header>
        <div class="topbar">
            <div class="container row">
                <nav class="menu">
                    <ul>
                        <li v-for="(item, index) in mainMenu" :key="index"><a :href="item.href">{{ item.text }}</a></li>
                    </ul>
                </nav>
                <div class="logo">
                    <img src="/boolean-logo.png" alt="Logo Boolean">
                </div>
                <nav class="menu2">
                    <a href="#"><i class="fa-regular fa-user"></i></a>
                    <a href="#"><i class="fa-regular fa-heart"></i></a>
                    <a href="#"><i class="fa-solid fa-bag-shopping"></i></a>
                </nav>
            </div>
        </div>
    </header>
</template>
  

  