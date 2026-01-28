<template>
  <div class="slidev-layout cover-layout">
    <!-- Logo top-left as per CD Manual -->
    <div class="logo-section">
      <img src="/Logo_Kanton_Luzern_RGB.svg" alt="Kanton Luzern" class="kl-logo" />
    </div>
    
    <!-- Content area -->
    <div class="content-area">
      <div class="content-wrapper">
        <h1 v-if="$slidev.configs.title" class="title">
          {{ $slidev.configs.title }}
        </h1>
        
        <h2 v-if="$slidev.configs.subtitle" class="subtitle">
          {{ $slidev.configs.subtitle }}
        </h2>
        
        <div class="metadata">
          <p v-if="$slidev.configs.author" class="author">
            {{ $slidev.configs.author }}
          </p>
          <p v-if="$slidev.configs.date" class="date">
            {{ $slidev.configs.date }}
          </p>
          <p v-if="$slidev.configs.department" class="department">
            {{ $slidev.configs.department }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Cover Layout
 * Clean, modern design as per CD Manual principles
 * Logo top-left, content centered
 */

.cover-layout {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background: white;
  position: relative;
  padding: 1.72rem; /* 1cm as per PowerPoint specs */
}

/* Logo Section - CD Manual: top-left, 10% of screen width */
.logo-section {
  position: absolute;
  top: 1.72rem;
  left: 1.72rem;
  z-index: 10;
}

.kl-logo {
  height: 1.72rem; /* 1cm height */
  width: auto;
}

/* Content Area */
.content-area {
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

/* Title Styling */
.title {
  font-size: 3.5rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 2rem;
  line-height: 1.2;
}

.subtitle {
  font-size: 2rem;
  font-weight: normal;
  color: #009FE3; /* Himmelblau */
  margin-bottom: 4rem;
  line-height: 1.3;
}

/* Metadata */
.metadata {
  margin-top: 4rem;
  font-size: 1.25rem;
  color: #333;
}

.author {
  font-weight: bold;
  margin-bottom: 0.5rem;
  color: #000;
}

.date {
  color: #666;
  margin-bottom: 0.5rem;
}

.department {
  color: #009FE3;
  font-weight: 600;
}

/* Responsive Design */
@media (max-width: 1024px) {
  .title {
    font-size: 2.5rem;
  }
  
  .subtitle {
    font-size: 1.5rem;
  }
  
  .content-area {
    padding: 4rem 2rem;
  }
}

@media (max-width: 768px) {
  .title {
    font-size: 2rem;
  }
  
  .subtitle {
    font-size: 1.25rem;
  }
}
</style>