<template>
  <div class="about">
    <div class="container">
      <h1>About Brian</h1>
      
      <section class="bio-section">
        <h2>Professional Background</h2>
        <p>
          Co-founder of PLANT PV, where I led the technical development of a revolutionary 
          "silver-on-aluminum" metallization paste for solar cell manufacturing. Our innovative 
          technology was successfully acquired by a Japanese multinational corporation in 2019, 
          marking a significant milestone in solar cell metallization advancement.
        </p>
      </section>

      <section class="bio-section">
        <h2>Education</h2>
        <p>
          I hold a PhD in Material Science and Engineering from Stanford University, where I 
          worked with Prof. Michael McGehee to develop cutting-edge solar cell architectures. 
          My academic journey also includes being a Swiss Fulbright scholar and Gilman Scholar, 
          reflecting my commitment to international collaboration in scientific research.
        </p>
        <p>
          I earned my BS in Electrical and Computer Engineering from the University of Texas 
          at Austin, providing me with a strong foundation in both the theoretical and practical 
          aspects of electrical systems and semiconductor technology.
        </p>
      </section>

      <section class="bio-section">
        <h2>Current Role</h2>
        <p>
          Currently, I serve as a Lecturer at Stanford University, where I co-teach a graduate 
          course on solar cells. Beyond classroom instruction, I am passionate about mentoring 
          students as they navigate their post-graduate school career paths, helping them 
          translate their academic achievements into meaningful professional opportunities.
        </p>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about {
  padding-top: 100px;
  min-height: 100vh;
  background-color: #f8f9fa;
}

.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 4rem 2rem;
}

h1 {
  font-size: 3rem;
  font-weight: 300;
  margin-bottom: 3rem;
  text-align: center;
  color: #333;
}

.bio-section {
  margin-bottom: 3rem;
  background: white;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.bio-section h2 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: #2c3e50;
  border-bottom: 2px solid #3498db;
  padding-bottom: 0.5rem;
}

.bio-section p {
  line-height: 1.7;
  color: #555;
  margin-bottom: 1rem;
  font-size: 1.1rem;
}

.bio-section p:last-child {
  margin-bottom: 0;
}

@media (max-width: 768px) {
  .container {
    padding: 2rem 1rem;
  }
  
  h1 {
    font-size: 2.5rem;
  }
  
  .bio-section {
    padding: 1.5rem;
  }
}
</style>