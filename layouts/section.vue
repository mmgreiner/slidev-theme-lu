<template>
  <div class="slidev-layout section-layout">
    <!-- Logo top-left -->
    <div class="logo-section">
      <img src="/Logo_Kanton_Luzern_RGB.svg" alt="Kanton Luzern" class="kl-logo" />
    </div>
    
    <!-- Section content centered -->
    <div class="section-content">
      <div class="section-wrapper">
        <slot />
      </div>
    </div>
  </div>
</template>

<style scoped>
/*
 * Section Layout
 * For chapter dividers and major transitions
 * Clean, impactful design
 */

.section-layout {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background: white;
  position: relative;
  padding: 1.72rem;
}

/* Logo */
.logo-section {
  position: absolute;
  top: 1.72rem;
  left: 1.72rem;
  z-index: 10;
}

.kl-logo {
  height: 1.72rem;
  width: auto;
}

/* Content */
.section-content {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 6rem 4rem;
}

.section-wrapper {
  max-width: 900px;
  text-align: center;
}

.section-wrapper :deep(h1) {
  font-size: 4rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 2rem;
  line-height: 1.1;
}

.section-wrapper :deep(h2) {
  font-size: 2.5rem;
  font-weight: normal;
  color: #009FE3; /* Himmelblau */
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.section-wrapper :deep(h3) {
  font-size: 1.5rem;
  font-weight: normal;
  color: #09202C; /* Mitternachtsblau */
  line-height: 1.3;
}

.section-wrapper :deep(p) {
  font-size: 1.25rem;
  line-height: 1.6;
  color: #333;
}

/* Responsive */
@media (max-width: 1024px) {
  .section-wrapper :deep(h1) {
    font-size: 3rem;
  }
  
  .section-wrapper :deep(h2) {
    font-size: 2rem;
  }
  
  .section-content {
    padding: 4rem 2rem;
  }
}

@media (max-width: 768px) {
  .section-wrapper :deep(h1) {
    font-size: 2.5rem;
  }
  
  .section-wrapper :deep(h2) {
    font-size: 1.5rem;
  }
}
</style>