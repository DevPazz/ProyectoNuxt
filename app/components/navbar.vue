<template>
	<nav class="nav">
		<NuxtLink to="/" class="brand">
			<span class="brand-mark">YPN</span>
			<div>
				<p class="brand-title">Mi Vlog</p>
				<p class="brand-subtitle">Historias, rutas y aprendizajes</p>
			</div>
		</NuxtLink>

		<div class="links">
			<NuxtLink to="/">Inicio</NuxtLink>
			<NuxtLink to="/about">Acerca de</NuxtLink>
		</div>
	</nav>
</template>

<style scoped>
.nav {
	display: flex;
	justify-content: space-between;
	align-items: center;
	backdrop-filter: blur(8px);
	background: rgba(15, 23, 42, 0.85);
	color: white;
	padding: 16px clamp(20px, 4vw, 44px);
	border-bottom: 1px solid rgba(255, 255, 255, 0.08);
	position: sticky;
	top: 0;
	z-index: 30;
}

.brand {
	display: flex;
	align-items: center;
	gap: 12px;
	text-decoration: none;
	color: inherit;
}

.brand-mark {
	width: 40px;
	height: 40px;
	border-radius: 12px;
	display: grid;
	place-items: center;
	font-weight: 700;
	background: linear-gradient(140deg, #f97316, #ef4444);
	box-shadow: 0 8px 20px rgba(239, 68, 68, 0.35);
}

.brand-title {
	margin: 0;
	font-size: 1.05rem;
	font-weight: 700;
	letter-spacing: 0.4px;
}

.brand-subtitle {
	margin: 0;
	font-size: 0.76rem;
	opacity: 0.8;
}

.links a {
	margin-left: 18px;
	color: white;
	text-decoration: none;
	font-weight: 600;
	padding: 8px 13px;
	border-radius: 999px;
	transition: 0.2s;
}

.links a:hover {
	background: rgba(255, 255, 255, 0.13);
	color: #fdba74;
}

.router-link-active {
	background: rgba(255, 255, 255, 0.16);
}

@media (max-width: 640px) {
	.brand-subtitle {
		display: none;
	}

	.links a {
		margin-left: 8px;
		padding: 7px 10px;
		font-size: 0.92rem;
	}
}
</style>