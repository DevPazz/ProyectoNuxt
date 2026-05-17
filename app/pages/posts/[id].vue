<script setup>

import { useRoute } from 'vue-router'
import { posts } from '../../data/posts'

const route = useRoute()

const post =
posts.find(
p => p.id == route.params.id
)

</script>



<template>

<section v-if="post" class="container">
<img :src="post.cover" :alt="post.title" class="hero-image" />

<div class="article">
<p class="meta">{{ post.date }} · {{ post.duration }} · {{ post.place }}</p>
<h1>{{ post.title }}</h1>
<p class="mood">Estado del dia: {{ post.mood }}</p>

<div class="tags">
<span v-for="tag in post.tags" :key="tag">#{{ tag }}</span>
</div>

<p
v-for="(paragraph, index) in post.content.split('\n\n')"
:key="index"
class="paragraph"
>
{{ paragraph }}
</p>

<NuxtLink
to="/"
class="btn"
>
Volver al inicio
</NuxtLink>
</div>
</section>

<section v-else class="not-found">
<h1>Post no encontrado</h1>
<p>El episodio que buscas no existe o fue removido.</p>
<NuxtLink to="/" class="btn">Volver al inicio</NuxtLink>
</section>

</template>



<style scoped>

.container {
	max-width: 980px;
	margin: auto;
	padding: 34px 22px;
}

.hero-image {
	width: 100%;
	max-height: 420px;
	object-fit: cover;
	border-radius: 22px;
	box-shadow: var(--shadow);
}

.article {
	margin-top: 16px;
	background: white;
	border-radius: 20px;
	border: 1px solid var(--line);
	padding: clamp(18px, 3vw, 30px);
	box-shadow: var(--shadow);
}

.meta {
	margin: 0;
	color: #6b7280;
	font-size: 0.9rem;
}

h1 {
	margin: 8px 0;
	font-family: 'DM Serif Display', serif;
	font-size: clamp(2rem, 5vw, 2.8rem);
	line-height: 1.1;
}

.mood {
	margin: 0;
	color: #1d4ed8;
	font-weight: 700;
}

.tags {
	display: flex;
	gap: 8px;
	flex-wrap: wrap;
	margin-top: 14px;
}

.tags span {
	padding: 4px 10px;
	background: #fff7ed;
	border: 1px solid #fed7aa;
	border-radius: 999px;
	font-size: 0.8rem;
	color: #9a3412;
}

.paragraph {
	margin-top: 16px;
	line-height: 1.75;
	color: #374151;
}

.btn {
	display: inline-block;
	margin-top: 24px;
	padding: 10px 18px;
	background: linear-gradient(140deg, #f97316, #ef4444);
	color: white;
	border-radius: 10px;
	text-decoration: none;
	font-weight: 700;
}

.not-found {
	max-width: 760px;
	margin: 40px auto;
	padding: 26px;
	text-align: center;
	background: white;
	border-radius: 20px;
	border: 1px solid var(--line);
}

</style>