<template>
	<section class="about-wrap">
		<div class="about-card">
			<p class="eyebrow">Detras de camara</p>
			<h1>Sobre este vlog</h1>

			<p>
				Este espacio nacio para documentar mi proceso real como estudiante y creador: dias buenos,
				dias pesados y pequenos avances que terminan siendo grandes cambios.
			</p>

			<p>
				Cada episodio mezcla rutina, aprendizaje y storytelling. La idea es compartir experiencias
				honestas que tambien te ayuden a organizarte, motivarte y crear tus propios proyectos.
			</p>

			<div class="facts">
				<article>
					<h2>Frecuencia</h2>
					<p>1 episodio nuevo por semana.</p>
				</article>
				<article>
					<h2>Formato</h2>
					<p>Vlogs cortos entre 5 y 10 minutos.</p>
				</article>
				<article>
					<h2>Temas</h2>
					<p>Estudio, creatividad, habitos y vida universitaria.</p>
				</article>
			</div>
		</div>
	</section>
</template>

<style scoped>
.about-wrap {
	max-width: 980px;
	margin: auto;
	padding: 38px 22px;
}

.about-card {
	background: #ffffff;
	border: 1px solid var(--line);
	border-radius: 22px;
	padding: clamp(20px, 3vw, 34px);
	box-shadow: var(--shadow);
	position: relative;
	overflow: hidden;
}

.about-card::before {
	content: '';
	position: absolute;
	right: -50px;
	top: -70px;
	width: 210px;
	height: 210px;
	border-radius: 50%;
	background: radial-gradient(circle at center, rgba(239, 68, 68, 0.2), transparent 70%);
}

.eyebrow {
	margin: 0;
	color: #c2410c;
	font-weight: 700;
}

h1 {
	font-family: 'DM Serif Display', serif;
	margin: 6px 0 16px;
	font-size: clamp(1.9rem, 5vw, 2.7rem);
}

p {
	color: #4b5563;
	line-height: 1.65;
}

.facts {
	margin-top: 22px;
	display: grid;
	gap: 12px;
	grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}

.facts article {
	border: 1px solid #fed7aa;
	background: #fff7ed;
	border-radius: 14px;
	padding: 14px;
}

h2 {
	margin: 0;
	font-size: 1rem;
}

.facts p {
	margin: 6px 0 0;
	font-size: 0.92rem;
}
</style>