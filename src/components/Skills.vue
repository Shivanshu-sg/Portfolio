<script setup>
const skillGroups = [
  {
    title: "AI / ML",
    skills: ["PyTorch", "scikit-learn", "LangChain", "Hugging Face", "Langgraph"]
  },
  {
    title: "Data & Analytics",
    skills: ["Pandas", "NumPy"]
  },
  {
    title: "Backend Development",
    skills: ["Python", "FastAPI", "Flask", "Docker"]
  },
  {
    title: "Frontend Development",
    skills: ["Vue.js"]
  },
  {
    title: "Collaboration & Deployment",
    skills: ["GitHub", "Docker"]
  },
  {
    title: "Cloud Development",
    skills: [
      "Google Cloud Platform",
      "VM Instances",
      "Cloud Run",
      "Cloud Build",
      "Cloud SQL",
      "Storage Buckets",
      "Firebase Hosting"
    ]
  }
]
</script>

<template>
  <section id="skills" class="skills-section">
    <div class="container">
      <div class="skills-shell">
        <div class="skills-header">
          <span class="section-label">Skills</span>
          <h2 class="skills-title">Technologies and tools I use to build practical, scalable solutions</h2>
          <p class="skills-intro">
            My skill set combines AI, backend engineering, cloud deployment, and product-focused development for
            building end-to-end applications.
          </p>
        </div>

        <div class="row g-4">
          <div v-for="group in skillGroups" :key="group.title" class="col-md-6 col-xl-4">
            <article class="skill-card">
              <h3 class="skill-card-title">{{ group.title }}</h3>

              <div class="skill-chip-list">
                <span v-for="skill in group.skills" :key="skill" class="skill-chip">
                  {{ skill }}
                </span>
              </div>
            </article>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
