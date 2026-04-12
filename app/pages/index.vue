<script setup>
import { posts } from '../data/posts'
</script>

<template>

  <div>
    <h1>Mini Blog con Nuxt</h1>

    <p>Ejemplo básico para demostrar el funcionamiento del framework</p>

    <div v-for="post in posts" :key="post.id">

      <h2>
        <NuxtLink :to="`/posts/${post.id}`">
          {{ post.title }}
        </NuxtLink>
      </h2>

    </div>

  </div>

</template>