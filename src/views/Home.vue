<template>
  <div class="home">
    <div class="hero-card">
      <div class="hero-content">
        <h1 class="hero-title">Specksnyder Labs</h1>
        <p class="hero-subtitle">Innovations in Clean Technology and Material Science</p>
      </div>
    </div>
    
    <div class="companies-section">
      <div class="company-cards">
        <a href="https://www.plantpv.com" target="_blank" class="company-card-link">
          <div class="company-card plant-pv-card">
            <img src="https://www.plantpv.com/wp-content/uploads/2021/05/cropped-cropped-PLANT-PV-Sign-300dpi-paint-scaled-1.jpg" alt="PLANT PV" class="company-logo">
            <p class="role">Co-Founder, President & Board Member</p>
            <p class="acquisition">Acquired in 2019</p>
            <div class="tooltip">
              PLANT PV developed silver metallization pastes that increased silicon solar cell efficiencies by 0.1%. PLANT PV was acquired by Hitachi Chemical in 2019.
            </div>
          </div>
        </a>
        <a href="https://photara.tech" target="_blank" class="company-card-link">
          <div class="company-card photara-card">
            <img src="../assets/images/photara_logo.png" alt="Photara" class="company-logo">
            <p class="role">Co-Founder, CEO & Board Member</p>
            <p class="acquisition">Active</p>
            <div class="tooltip">
              Photara develops equipment and consumables to replace silver with base metals on silicon solar cells.
            </div>
          </div>
        </a>
        <a href="https://www.khemiametals.com" target="_blank" class="company-card-link">
          <div class="company-card khemia-card">
            <img src="../assets/images/khemia_temp_logo.png" alt="Khemia" class="company-logo khemia-logo">
            <p class="role">Co-Founder, Board Member</p>
            <p class="acquisition">Active</p>
            <div class="tooltip">
              Khemia develops base metal alloy foils to replace copper foil in lithium-ion batteries.
            </div>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import bigsurImage from '../assets/images/Bigsur1.jpg'

export default {
  name: 'Home',
  data() {
    return {
      bigsurImage
    }
  }
}
</script>

<style scoped>
.home {
  min-height: 100vh;
  padding: 120px 2rem 4rem;
  background-color: #f8f9fa;
}

.hero-card {
  max-width: 1200px;
  margin: 0 auto 4rem;
  height: 400px;
  background-image: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),
                    url('../assets/images/Bigsur1.jpg');
  background-size: cover;
  background-position: center;
  border-radius: 12px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
  overflow: hidden;
}

.hero-content {
  max-width: 800px;
  padding: 2rem;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 300;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.hero-subtitle {
  font-size: 1.3rem;
  font-weight: 300;
  opacity: 0.9;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.companies-section {
  max-width: 1200px;
  margin: 0 auto;
}

.company-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  transition: gap 0.3s ease;
}

@media (max-width: 1024px) {
  .company-cards {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .company-card-link:hover ~ .company-card-link {
    transform: translateY(140px);
  }
  
  .company-card-link:hover ~ .company-card-link .company-card {
    transition: transform 0.3s ease;
  }
  
  .company-card-link {
    transition: transform 0.3s ease;
  }
}

.company-card {
  background: white;
  border-radius: 12px;
  padding: 3rem 2rem;
  text-align: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
  height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.company-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}

.company-card h3 {
  font-size: 1.8rem;
  font-weight: 600;
  color: #2c3e50;
  margin: 0 0 1rem 0;
  flex-shrink: 0;
}

.company-card .role {
  font-size: 1rem;
  color: #666;
  font-weight: 400;
  line-height: 1.4;
  margin: 0;
}

.company-card .acquisition {
  font-size: 0.95rem;
  color: #888;
  font-weight: 400;
  font-style: italic;
  line-height: 1.4;
  margin: 0.5rem 0 0 0;
}

.company-logo {
  max-width: 180px;
  height: 60px;
  width: auto;
  margin-bottom: 1rem;
  object-fit: contain;
  flex-shrink: 0;
}

.khemia-logo {
  height: 60px;
  max-width: 180px;
  width: auto;
}

.company-card-link {
  text-decoration: none;
  display: block;
  position: relative;
}


.plant-pv-card,
.photara-card,
.khemia-card {
  position: relative;
  overflow: visible;
}

.tooltip {
  position: absolute;
  top: 220px;
  left: 50%;
  transform: translateX(-50%);
  background: white;
  color: #333;
  padding: 12px 16px;
  border-radius: 8px;
  font-size: 0.9rem;
  line-height: 1.4;
  width: 280px;
  min-height: 60px;
  text-align: center;
  opacity: 0;
  visibility: hidden;
  transition: opacity 0.3s ease, visibility 0.3s ease;
  z-index: 1000;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  border: 1px solid #e0e0e0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.tooltip::before {
  content: '';
  position: absolute;
  top: -6px;
  left: 50%;
  transform: translateX(-50%);
  width: 0;
  height: 0;
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-bottom: 6px solid white;
}

.plant-pv-card:hover .tooltip,
.photara-card:hover .tooltip,
.khemia-card:hover .tooltip {
  opacity: 1;
  visibility: visible;
}


.overlay-tooltip::before {
  display: none;
}

@media (max-width: 768px) {
  .home {
    padding: 100px 1rem 2rem;
  }
  
  .hero-card {
    height: 300px;
    margin-bottom: 2rem;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-subtitle {
    font-size: 1.1rem;
  }
  
  .company-cards {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .company-card {
    padding: 2rem 1.5rem;
    min-height: 200px;
  }
  
  .tooltip {
    width: calc(100vw - 2rem);
    max-width: 320px;
    font-size: 1rem;
    padding: 16px;
  }
  
  .company-card-link:hover ~ .company-card-link {
    transform: translateY(140px);
  }
}

@media (max-width: 480px) {
  .home {
    padding: 90px 0.5rem 2rem;
  }
  
  .hero-card {
    height: 250px;
    margin: 0 0.5rem 2rem;
  }
  
  .hero-title {
    font-size: 2rem;
  }
  
  .hero-subtitle {
    font-size: 1rem;
  }
  
  .company-card {
    padding: 1.5rem 1rem;
    margin: 0 0.5rem;
  }
  
  .company-logo {
    height: 50px;
  }
  
  .khemia-logo {
    height: 50px;
  }
  
  .role {
    font-size: 0.9rem;
  }
  
  .acquisition {
    font-size: 0.85rem;
  }
  
  .tooltip {
    width: calc(100vw - 1rem);
    max-width: 280px;
    font-size: 0.9rem;
    padding: 12px;
    line-height: 1.3;
  }
  
  .nav-logo {
    height: 32px;
  }
  
  .navbar {
    padding: 0.75rem 0;
  }
  
  .nav-container {
    padding: 0 1rem;
  }
}
</style>