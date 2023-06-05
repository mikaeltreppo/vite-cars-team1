<template>
//<div class="card m-3"  style="width: 18rem;">
    <div class="card-body">
        <img src="https://picsum.photos/200/300" class="card-img-top" alt="...">
        <h5 class="card-title">{{ data.brand}}</h5>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ data.model }}</h6>
        <p class="card-text">{{ data.price }}</p>
        <!-- <router-link :to="{name: 'singleproject', params: {id: car.id}}" class="btn btn-primary">
            Vedi post completo
        </router-link> -->

    </div>
</div>
</template>
<script>
export default{
    name: 'MyCard',
    props: {
        data: Array,
    }
}
</script>
