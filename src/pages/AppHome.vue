<template>
    <div class="container">
        <MyCard v-for="car in cars" :data="car" :key="car.id"></MyCard>
    </div>
</template>
<script>

import axios from 'axios';
import { store } from '../../store';
import MyCard from '../components/MyCard.vue';

export default {
    components: {
        MyCard,

    },
    data() {
        return {
            cars: [],
            store,
            currentPage: 1,
            lastPage: null
        }
    },
    methods: {
        getCard() {
            axios.get(`${this.store.baseUrl}/api/cars`).then(response => {

                this.cars = response.data.results.data;
                this.currentPage = response.data.results.current_page;
                this.lastPage = response.data.results.last_page;

                console.log(this.cars)
            });
        }
    }, 
    mounted() {
        if(this.cars.length==0){
        this.getCard()};
    }
}

</script>
<style lang="scss"></style>
