<template>
  <main>
    <section id="sobre-mi">
      <h2>
        <img :src="circleUserIcon" alt="icono">
        Sobre mi
      </h2>
      <p>¡Hola! Soy Magali Ordenes Viguet, una desarrolladora enfocado en modularidad, eficiencia y experiencia de usuario. Me encanta escribir código limpio, lógico y bien organizado.</p>
    </section>
    
    <section id="experiencia">
      <h2>
        <img :src="briefcaseIcon" alt="icono">
        Experiencia
      </h2>
      <ul>
        <li>Desarrollo de sistemas de reservas con PSeInt y JavaScript. Conocimientos en Java y Python.</li>
        <li>Optimización y mantenimiento de código HTML y CSS</li>
      </ul>
    </section>
    
    <section id="estudios">
      <h2>
        <img :src="universityIcon" alt="icono">
        Estudios
      </h2>
      <p>Formación en programación, lógica computacional, y metodologías ágiles como Scrum.</p>
    </section>
    
    <section id="proyectos">
      <h2>
        <img :src="folderIcon" alt="icono">
        Proyectos
      </h2>
      <ul>
        <li>Software de reserva de entradas para cine</li>
        <li>Dashboard de cálculo automático en Excel</li>
      </ul>
    </section>
    
    <section id="contactame">
      <h2>
        <img :src="phoneIcon" alt="icono">
        Contactame
      </h2>
      <p>Siéntete libre de contactarme a <strong>magali.ordenesviguet@gmail.com</strong> o conectarte vía LinkedIn.</p>
    </section>
  </main>
</template>

<script>
import circleUserIcon from '../assets/icons/circle-user-svgrepo-com.svg'
import briefcaseIcon from '../assets/icons/briefcase-alt-svgrepo-com.svg'
import universityIcon from '../assets/icons/university-svgrepo-com.svg'
import folderIcon from '../assets/icons/folder-svgrepo-com.svg'
import phoneIcon from '../assets/icons/phone-svgrepo-com.svg'

export default {
  name: 'MainContent',
  data() {
    return {
      circleUserIcon,
      briefcaseIcon,
      universityIcon,
      folderIcon,
      phoneIcon
    }
  }
}
</script>

<style scoped>
main {
  max-width: 900px;
  margin: 2rem auto;
  padding: 0 1.5rem;
  flex: 1;
}

section {
  margin-bottom: 3rem;
  background-color: white;
  padding: 1.5rem;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.05);
  transition: transform 0.3s ease;
}

section:hover {
  transform: translateY(-5px);
}

section h2 {
  font-size: 1.6rem;
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--violeta-oscuro);
  border-bottom: 2px solid var(--coral-pastel);
  padding-bottom: 0.5rem;
}

section h2 img {
  width: 26px;
  height: 26px;
}

section p, section ul {
  padding: 1rem;
  line-height: 1.6;
}

ul {
  list-style: none;
  padding-left: 1rem;
}

ul li {
  position: relative;
  margin-bottom: 0.5rem;
  padding-left: 1.5rem;
}

ul li::before {
  content: "•";
  color: var(--coral-pastel);
  font-weight: bold;
  position: absolute;
  left: 0;
}
</style>