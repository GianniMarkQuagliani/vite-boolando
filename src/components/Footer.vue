<script>
import userMenu from '../data/userMenu';
  export default {
    name: 'Footer',
    data () {
        return {
            userMenu
        }
    }
};
</script>
  
<template>
    <footer>
        <div class="container row">
            <nav class="copyright">
                <h5 class="name-company">Booleando s.r.l</h5>
                <ul>
                    <li v-for="(item, index) in userMenu" :key="index"><a :href="item.href">{{ item.text }}</a></li>
                </ul>
            </nav>
        </div>
        <nav class="social">
            <h5>Trovaci anche su</h5>
            <a href="#"><i class="fa-brands fa-square-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-facebook"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
            <a href="#"><i class="fa-brands fa-pinterest-p"></i></a>
            <a href="#"><i class="fa-brands fa-square-youtube"></i></a>
        </nav>
    </footer>
</template>