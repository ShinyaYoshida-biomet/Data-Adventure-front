<template>
  <div class="top">
    <transition name="fade">
      <div v-if="show" class="top__message">
        <h1>Welcome to this wonderful data analysis world!!</h1>
      </div>
    </transition>
    <div class="top__cards">
      <v-card class="top__cards--card" elevation="10" to="/wine">
        <v-img height="200px" src="wine.jpg" />
        <v-card-title class="top__cards--title">
          Wine
        </v-card-title>
      </v-card>

      <v-card class="top__cards--card" elevation="10" to="/iris">
        <v-img height="200px" src="iris.jpg" />
        <v-card-title class="top__cards--title">
          Iris
        </v-card-title>
      </v-card>
      <v-card class="top__cards--card" elevation="10" to="/diabetes">
        <v-img height="200px" src="diabetes.jpg" />
        <v-card-title class="top__cards--title">
          Diabetes
        </v-card-title>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      show: false
    }
  },
  mounted () {
    this.show = true
  }
}
</script>

<style lang="scss" scoped>
.fade-enter {
  opacity: 0;
}
.fade-enter-active {
  transition: 5s;
}
.fade-enter-to {
  opacity: 1;
}
.fade-leave {
  opacity: 1;
}
.fade-leave-active {
  transition: 5s;
}
.fade-leave-to {
  opacity: 0;
}
.top {
  text-align: center;
  &__message {
    font-size: 40px;
    margin: 30px auto;
  }
  &__cards {
    display: flex;
    &--card {
      height: 350px;
      margin: 10% auto;
      width: 300px;
    }
    &--title {
      font-size: 30px;
      justify-content: center;
    }
  }
}
</style>
