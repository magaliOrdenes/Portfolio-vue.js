<template>
  <footer>
    <div class="footer-social">
      <a href="https://github.com/magaliOrdenes" target="_blank">
        <img :src="githubIcon" alt="GitHub">
        GitHub
      </a>
      <a href="https://www.linkedin.com/in/magali-ordenes-viguet-2953532b3/" target="_blank">
        <img :src="linkedinIcon" alt="LinkedIn">
        LinkedIn
      </a>
    </div>
    <div class="footer-legal">
      © 2025. Magali Ordenes Viguet – Grupo Los Idos – Portfolio Web – Todos los derechos reservados.
    </div>
  </footer>
</template>

<script>
import githubIcon from '../assets/icons/github-142-svgrepo-com.svg'
import linkedinIcon from '../assets/icons/linkedin-rounded-svgrepo-com.svg'

export default {
  name: 'Footer',
  data() {
    return {
      githubIcon,
      linkedinIcon
    }
  }
}
</script>

<style scoped>
.footer-social {
  background-color: var(--violeta-oscuro);
  padding: 1.5rem;
  display: flex;
  justify-content: center;
  gap: 3rem;
}

.footer-social a {
  color: white;
  display: flex;
  align-items: center;
  text-decoration: none;
  gap: 0.5rem;
  font-weight: 600;
  transition: transform 0.3s ease;
  padding: 0.5rem 1rem;
  border-radius: 5px;
}

.footer-social a:hover {
  transform: scale(1.1);
  background-color: rgba(255,255,255,0.1);
}

.footer-social img {
  width: 22px;
  height: 22px;
  filter: brightness(0) invert(1);
}

.footer-legal {
  background-color: var(--violeta-pastel);
  text-align: center;
  padding: 1rem;
  font-size: 0.9rem;
  color: var(--texto-oscuro);
}

@media (max-width: 768px) {
  .footer-social {
    flex-direction: column;
    gap: 1rem;
    align-items: center;
  }
}
</style>