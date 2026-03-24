<script setup>
const projects = [
  {
    title: "NeuroMate: Privacy-Preserving Genetic Disease AI Assistant",
    category: "AI Product",
    description:
      "A privacy-focused medical information assistant designed to make complex genetic disease knowledge easier for patients to understand.",
    problem:
      "Patients with genetic diseases often struggle to understand complex medical information and have limited time with doctors.",
    solution:
      "Developing a RAG-based AI agent that retrieves reliable medical knowledge and converts it into simple, understandable answers. The system is designed to run locally to ensure data privacy and security.",
    impact:
      "Makes critical health information more accessible while maintaining user trust through private, secure interactions and accurate medical citations.",
    tech: ["LLMs", "RAG", "FastAPI"],
    status: "In Progress",
    outcome: "Focused on making technical healthcare information easier to understand and navigate.",
    ctaLabel: "View Details",
    ctaHref: "https://github.com/Shivanshu-sg/NeuroMate"
  },
  {
    title: "Crop Disease Prediction",
    category: "Computer Vision",
    description:
      "A machine learning project built during the Annam.ai Hackathon to identify crop diseases from image inputs.",
    problem:
      "Farmers and agricultural teams often face delays in identifying crop diseases, which can lead to reduced yield and slower response times.",
    solution:
      "Developed a computer vision model during the Annam.ai Hackathon to classify crop diseases from image inputs and support faster initial diagnosis.",
    impact:
      "Showcased how image-based disease detection can help make agricultural support more efficient and improve early decision-making.",
    tech: ["PyTorch", "Computer Vision", "Image Classification"],
    status: "Completed",
    outcome: "Built to support faster identification of crop issues through image-based analysis.",
    ctaLabel: "View Details",
    ctaHref: "#"
  }
]
</script>

<template>
  <section id="projects" class="projects-section">
    <div class="container">
      <div class="projects-shell">
        <div class="projects-header">
          <span class="section-label">Projects</span>
          <h2 class="projects-title">A few projects that reflect how I build, learn, and solve problems</h2>
          <p class="projects-intro">
            These projects highlight my interest in AI systems, backend development, and practical products built
            around real use cases.
          </p>
        </div>

        <div class="row g-4">
          <div v-for="project in projects" :key="project.title" class="col-lg-6">
            <article class="project-card">
              <div class="project-card-top">
                <span class="project-category">{{ project.category }}</span>
                <span
                  class="project-status"
                  :class="{ 'project-status-active': project.status === 'In Progress' }"
                >
                  {{ project.status }}
                </span>
              </div>

              <h3 class="project-title">{{ project.title }}</h3>
              <p class="project-description">{{ project.description }}</p>

              <div v-if="project.problem || project.solution || project.impact" class="project-case-study">
                <div v-if="project.problem" class="project-case-block">
                  <span class="project-case-label">Problem</span>
                  <p>{{ project.problem }}</p>
                </div>

                <div v-if="project.solution" class="project-case-block">
                  <span class="project-case-label">Solution</span>
                  <p>{{ project.solution }}</p>
                </div>

                <div v-if="project.impact" class="project-case-block">
                  <span class="project-case-label">Impact</span>
                  <p>{{ project.impact }}</p>
                </div>
              </div>

              <div class="project-tech-list">
                <span v-for="tech in project.tech" :key="tech" class="project-tech-chip">
                  {{ tech }}
                </span>
              </div>

              <div class="project-footer">
                <p class="project-outcome">{{ project.outcome }}</p>
                <a :href="project.ctaHref" class="project-link">{{ project.ctaLabel }}</a>
              </div>
            </article>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
