<template>
  <header>
    <div class="perfil">
      <img :src="profileImage" alt="Foto de Magali Ordenes">
      <div class="info-perfil">
        <h1>Magali Ordenes</h1>
        <h2>Técnica en Programación</h2>
      </div>
    </div>
    <nav>
      <a v-for="item in navItems" :key="item.id" :href="item.href" class="nav-btn">
        <img :src="item.icon" :alt="item.alt">
        {{ item.text }}
      </a>
    </nav>
  </header>
</template>

<script>
import profileImage from '../assets/images/CV foto.jpeg'
import circleUserIcon from '../assets/icons/circle-user-svgrepo-com.svg'
import briefcaseIcon from '../assets/icons/briefcase-alt-svgrepo-com.svg'
import universityIcon from '../assets/icons/university-svgrepo-com.svg'
import folderIcon from '../assets/icons/folder-svgrepo-com.svg'
import phoneIcon from '../assets/icons/phone-svgrepo-com.svg'

export default {
  name: 'Header',
  data() {
    return {
      profileImage,
      navItems: [
        { id: 1, href: '#sobre-mi', icon: circleUserIcon, alt: 'icono', text: 'Sobre mi' },
        { id: 2, href: '#experiencia', icon: briefcaseIcon, alt: 'icono', text: 'Experiencia' },
        { id: 3, href: '#estudios', icon: universityIcon, alt: 'icono', text: 'Estudios' },
        { id: 4, href: '#proyectos', icon: folderIcon, alt: 'icono', text: 'Proyectos' },
        { id: 5, href: '#contactame', icon: phoneIcon, alt: 'icono', text: 'Contactame' }
      ]
    }
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 2rem;
  flex-wrap: wrap;
  background-color: var(--violeta-pastel);
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.perfil {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.perfil img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid var(--coral-pastel);
}

.info-perfil h1 {
  font-size: 1.8rem;
  margin-bottom: 0.2rem;
  color: var(--texto-oscuro);
}

.info-perfil h2 {
  font-size: 1.2rem;
  font-weight: 400;
  color: var(--violeta-oscuro);
}

nav {
  display: flex;
  gap: 0.8rem;
  flex-wrap: wrap;
}

.nav-btn {
  display: flex;
  align-items: center;
  gap: 0.4rem;
  background-color: var(--coral-pastel);
  color: var(--texto-oscuro);
  padding: 0.7rem 1.2rem;
  border-radius: 30px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: relative;
  overflow: hidden;
}

.nav-btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
  transition: left 0.5s;
}

.nav-btn:hover {
  background-color: var(--violeta-pastel);
  transform: translateY(-3px);
  box-shadow: 0 6px 12px rgba(0,0,0,0.15);
}

.nav-btn:hover::before {
  left: 100%;
}

.nav-btn img {
  width: 20px;
  height: 20px;
}

@media (max-width: 768px) {
  header {
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
    text-align: center;
  }
  
  .perfil {
    flex-direction: column;
  }
  
  nav {
    justify-content: center;
  }
  
  .nav-btn {
    flex: 1;
    min-width: 150px;
    justify-content: center;
  }
}
</style>