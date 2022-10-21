<script setup>
const props = defineProps(['productData'])
</script>

<template>
  <div class="card mb-3" style="max-width: 540px;">
    <div class="row g-0">
      <div class="col-md-4">
        <img v-bind:src="productData.image" class="img-fluid rounded-start" alt="...">
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title">{{ productData.title }}</h5>
          <p class="card-text">{{ productData.description }}</p>
          <p class="card-text"><small class="text-muted">{{ productData.price }}</small></p>
        </div>
      </div>
    </div>
  </div>
</template>