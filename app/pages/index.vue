<script setup>

import { posts } from '../data/posts'

</script>


<template>

<section class="hero">
<p class="badge">Nuevo episodio cada semana</p>
<h1>Blog Personal</h1>
<p class="intro">
Historias reales de estudio, ideas creativas y momentos cotidianos convertidos en episodios.
</p>
</section>

<section class="container">
<div class="grid">
<article
v-for="post in posts"
:key="post.id"
class="card"
>
<img :src="post.cover" :alt="post.title" class="cover" />

<div class="card-body">
<p class="meta">{{ post.date }} · {{ post.duration }}</p>
<h2>{{ post.title }}</h2>
<p class="excerpt">{{ post.excerpt }}</p>
<p class="place">Lugar: {{ post.place }}</p>

<div class="tags">
<span v-for="tag in post.tags" :key="tag">#{{ tag }}</span>
</div>

<NuxtLink
:to="`/posts/${post.id}`"
class="btn"
>
Ver episodio
</NuxtLink>
</div>
</article>
</div>
</section>

</template>



<style scoped>

.hero {
	max-width: 1050px;
	margin: 0 auto;
	padding: clamp(28px, 5vw, 54px) 22px 18px;
}

.badge {
	display: inline-block;
	margin: 0;
	padding: 8px 14px;
	border-radius: 999px;
	background: rgba(239, 68, 68, 0.13);
	color: #b91c1c;
	font-weight: 700;
	font-size: 0.86rem;
}

h1 {
	font-family: 'DM Serif Display', serif;
	font-size: clamp(2.1rem, 6vw, 3.2rem);
	line-height: 1.05;
	margin: 14px 0 10px;
	color: #111827;
}

.intro {
	max-width: 720px;
	margin: 0;
	color: #4b5563;
	font-size: 1.03rem;
}

.container {
	padding: 14px 22px 30px;
	max-width: 1050px;
	margin: auto;
}

.grid {
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
	gap: 22px;
}

.card {
	background: white;
	border-radius: 20px;
	overflow: hidden;
	box-shadow: var(--shadow);
	border: 1px solid var(--line);
	transition: transform 0.25s ease;
	animation: fade 0.55s ease;
}

.card:hover {
	transform: translateY(-7px);
}

.cover {
	width: 100%;
	height: 180px;
	object-fit: cover;
}

.card-body {
	padding: 18px;
}

.meta {
	margin: 0;
	color: #6b7280;
	font-size: 0.85rem;
}

h2 {
	margin: 10px 0;
	font-size: 1.2rem;
}

.excerpt {
	margin: 0;
	color: #4b5563;
}

.place {
	margin: 12px 0 10px;
	color: #1d4ed8;
	font-size: 0.92rem;
	font-weight: 600;
}

.tags {
	display: flex;
	flex-wrap: wrap;
	gap: 8px;
}

.tags span {
	padding: 4px 10px;
	background: #fff7ed;
	border: 1px solid #fed7aa;
	border-radius: 999px;
	font-size: 0.78rem;
	color: #9a3412;
}

.btn {
	display: inline-block;
	margin-top: 14px;
	padding: 10px 16px;
	background: linear-gradient(140deg, #f97316, #ef4444);
	color: white;
	border-radius: 10px;
	text-decoration: none;
	font-weight: 700;
}

@keyframes fade {
	from {
		opacity: 0;
		transform: translateY(14px);
	}

	to {
		opacity: 1;
		transform: translateY(0);
	}
}
</style>