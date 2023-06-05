<template>
//<div class="card m-3"  style="width: 18rem;">
    <div class="card-body">
        <img src="https://picsum.photos/200/300" class="card-img-top" alt="...">
        <h5 class="card-title">{{ car.brand}}</h5>
        <h6 class="card-subtitle mb-2 text-body-secondary">{{ car.author }}</h6>
        <p class="card-text">{{ car.description }}</p>
        <router-link :to="{name: 'singleproject', params: {id: car.id}}" class="btn btn-primary">
            Vedi post completo
        </router-link>

    </div>
</div>
</template>
<script>
export default{
    name: 'MyCard'
}
</script>
