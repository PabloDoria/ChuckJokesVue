<template>
  <div class="col-md-4 mb-4">
    <div class="card h-100 border-dark shadow">
      <img :src="iconUrl" class="card-img-top chuck-img" alt="Chuck Norris">
      <div class="card-body d-flex flex-column justify-content-between">
        <p class="card-text text-center">{{ value }}</p>
        <button 
          class="btn btn-danger btn-sm mt-2 align-self-end" 
          :class="{ 'btn-success': liked }" 
          @click="toggleLike"
        >
          <i class="fas fa-heart mr-1"></i> {{ liked ? 'Me gusta' : '¿Te gusta?' }}
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChuckCard',
  props: {
    iconUrl: String,
    value: String
  },
  data() {
    return {
      liked: false
    };
  },
  methods: {
    toggleLike() {
      this.liked = !this.liked;
    }
  }
}
</script>

<style scoped>
.chuck-img {
  border-bottom: 2px solid #dc3545;
  width: 100%;
  height: 350px;
  object-fit: cover;
}

.card {
  transition: transform 0.3s ease-in-out;
}

.card:hover {
  transform: translateY(-5px);
}
</style>
