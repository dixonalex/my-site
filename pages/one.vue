<template>
  <div class="">
    What's goouda
    <button @click="$store.commit('increment')">{{ $store.state.counter }}</button>
    <button @click="$store.commit('decrement')">{{ $store.state.counter }}</button>
  </div>
</template>
