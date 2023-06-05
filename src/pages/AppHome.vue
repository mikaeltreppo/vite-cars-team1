<template>
    <div class="container">
        <MyCard></MyCard>
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

                console.log(this.cars)
            });
         }}}
</script>
<style lang="scss"></style>
