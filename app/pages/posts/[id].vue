<script setup>

import { useRoute } from 'vue-router'
import { posts } from '../../data/posts'

const route = useRoute()

const post = posts.find(p => p.id == route.params.id)

</script>


<template>

<div>

<h1>{{ post.title }}</h1>

<p>{{ post.content }}</p>

<NuxtLink to="/">Volver al inicio</NuxtLink>

</div>

</template>