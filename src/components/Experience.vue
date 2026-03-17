<script setup>
const experienceProjects = [
  {
    title: "AI Order Extraction System",
    description:
      "Engineered a multimodal AI pipeline that automated the transition from social commerce conversations to structured order data. Integrated Whisper and Indic Conformer for multilingual speech-to-text, alongside LLMs for image and text understanding, to convert unstructured WhatsApp messages into validated order formats. The system reduced manual data entry by mapping natural language customer inputs to internal product schemas with high precision.",
    stack: ["Indic Conformer", "LLMs", "LangChain", "Meta Cloud API", "FastAPI", "Google Cloud", "Vue.js"]
  },
  {
    title: "Order & Delivery Management Platform",
    description:
      "Architected and deployed a full-stack enterprise platform to manage the end-to-end lifecycle of every order. Built with FastAPI and Vue.js, the system included a robust RBAC framework with dedicated interfaces for admins, operators, and delivery agents. Managed deployment on Google Cloud Platform using Cloud Run and Firebase for hosting, Cloud Build for CI/CD, and Cloud SQL (PostgreSQL) for scalable data management.",
    stack: ["FastAPI", "Vue.js", "RBAC", "Google Cloud", "Cloud Run", "Firebase", "Cloud Build", "Cloud SQL"]
  }
]
</script>

<template>
  <section id="experience" class="experience-section">
    <div class="container">
      <div class="experience-shell">
        <div class="experience-header">
          <span class="section-label">Experience</span>
          <h2 class="experience-title">Hands-on experience building AI systems and delivery-focused platforms</h2>
          <p class="experience-intro">
            During my internship at Nature's Soul, I worked on production-oriented systems that combined AI,
            backend engineering, and cloud deployment to solve operational problems.
          </p>
        </div>

        <div class="experience-card">
          <div class="experience-timeline">
            <span class="experience-dot"></span>
          </div>

          <div class="experience-content">
            <div class="experience-topline">
              <span class="experience-tag">Internship</span>
            </div>

            <div class="experience-heading">
              <div>
                <h3>AI Developer Intern</h3>
                <p>Nature's Soul</p>
              </div>
            </div>

            <div class="experience-projects">
              <article v-for="project in experienceProjects" :key="project.title" class="experience-project-card">
                <h4 class="experience-project-title">{{ project.title }}</h4>
                <p class="experience-project-description">{{ project.description }}</p>

                <div class="experience-stack">
                  <span class="experience-stack-label">Tech Stack</span>
                  <div class="experience-stack-list">
                    <span v-for="item in project.stack" :key="item" class="experience-stack-chip">
                      {{ item }}
                    </span>
                  </div>
                </div>
              </article>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
