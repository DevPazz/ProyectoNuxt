<script setup>

import Navbar from './components/navbar.vue'
import Footer from './components/footer.vue'

</script>


<template>

<div class="app-shell">

<Navbar />

<main class="main-content">
<NuxtPage />
</main>

<Footer />

</div>

</template>



<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&family=DM+Serif+Display:ital@0;1&display=swap');

:root {
	--bg-ink: #0f172a;
	--bg-cream: #fffaf3;
	--bg-sky: #ecfeff;
	--surface: #ffffff;
	--text-main: #1f2937;
	--text-soft: #5b6474;
	--accent: #ef4444;
	--accent-soft: #f97316;
	--line: rgba(15, 23, 42, 0.1);
	--shadow: 0 16px 35px rgba(15, 23, 42, 0.12);
}

* {
	box-sizing: border-box;
}

html,
body,
#__nuxt {
	margin: 0;
	min-height: 100%;
}

body {
	font-family: 'Space Grotesk', sans-serif;
	color: var(--text-main);
	background:
		radial-gradient(circle at 12% 15%, rgba(239, 68, 68, 0.15), transparent 35%),
		radial-gradient(circle at 90% 10%, rgba(249, 115, 22, 0.2), transparent 40%),
		linear-gradient(160deg, var(--bg-sky) 0%, var(--bg-cream) 55%, #ffffff 100%);
}

a {
	color: inherit;
}

.app-shell {
	min-height: 100vh;
	display: flex;
	flex-direction: column;
}

.main-content {
	flex: 1;
}
</style>