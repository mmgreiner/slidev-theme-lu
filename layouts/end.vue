<template>
  <div class="slidev-layout end-layout">
    <!-- Logo -->
    <div class="logo-section">
      <img src="/Logo_Kanton_Luzern_RGB.svg" alt="Kanton Luzern" class="kl-logo" />
    </div>
    
    <!-- Content centered -->
    <div class="content-section">
      <div class="content-wrapper">
        <slot />
        
        <div v-if="$slidev.configs.website" class="website">
          <a :href="$slidev.configs.website" target="_blank">
            {{ $slidev.configs.website }}
          </a>
        </div>
        
        <div v-if="$slidev.configs.contact" class="contact">
          {{ $slidev.configs.contact }}
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.end-layout {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background: white;
  position: relative;
  padding: 1.72rem;
}

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

.content-section {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 6rem 4rem;
}

.content-wrapper {
  max-width: 900px;
  text-align: center;
}

.content-wrapper :deep(h1) {
  font-size: 3.5rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 2rem;
  line-height: 1.1;
}

.content-wrapper :deep(h2) {
  font-size: 2rem;
  font-weight: normal;
  color: #009FE3; /* Himmelblau */
  margin-bottom: 2rem;
  line-height: 1.3;
}

.content-wrapper :deep(p) {
  font-size: 1.25rem;
  line-height: 1.6;
  color: #333;
  margin-bottom: 1rem;
}

.website {
  margin-top: 3rem;
  font-size: 1.25rem;
}

.website a {
  color: #009FE3;
  text-decoration: none;
  transition: opacity 0.2s ease;
  border-bottom: 2px solid #009FE3;
  padding-bottom: 2px;
}

.website a:hover {
  opacity: 0.8;
}

.contact {
  margin-top: 2rem;
  font-size: 1.125rem;
  color: #666;
  line-height: 1.6;
}

@media (max-width: 1024px) {
  .content-wrapper :deep(h1) {
    font-size: 2.5rem;
  }
  
  .content-wrapper :deep(h2) {
    font-size: 1.5rem;
  }
  
  .content-section {
    padding: 4rem 2rem;
  }
}
</style>