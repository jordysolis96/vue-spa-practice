<script setup>
const props = defineProps(['productData'])

</script>

<template>
  <div class="card mb-3" style="max-width: 540px;" v-for="product in productData" :key="product.id">
    <div class="row g-0">
      <div class="col-md-4">
        <img v-bind:src="product.image" class="img-fluid rounded-start" alt="...">
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title">{{ product.title }}</h5>
          <p class="card-text">{{ product.description }}</p>
          <p class="card-text"><small class="text-muted">{{ product.price }}</small></p>
        </div>
      </div>
    </div>
  </div>
</template>