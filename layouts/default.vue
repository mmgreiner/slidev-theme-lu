<template>
  <div class="slidev-layout default-layout">
    <!-- Logo top-left (CD Manual standard) -->
    <div class="header">
      <img src="/Logo_Kanton_Luzern_RGB.svg" alt="Kanton Luzern" class="header-logo" />
    </div>
    
    <!-- Main content area - aligned to logo as per CD rules -->
    <div class="content">
      <slot />
    </div>
    
    <!-- Footer with page number -->
    <div class="footer">
      <div class="footer-content">
        <div class="footer-left">
          <span v-if="$slidev.configs.department">{{ $slidev.configs.department }}</span>
        </div>
        <div class="footer-right">
          <span class="page-number">{{ $slidev.nav.currentPage }} / {{ $slidev.nav.total }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/*
 * Default Content Layout
 * Following CD Manual: simple, clean, functional
 * Logo at top-left, content aligned
 */

.default-layout {
  width: 100%;
  height: 100%;
  padding: 0;
  display: flex;
  flex-direction: column;
  background: white;
  color: #000;
}

/* Header with Logo - CD Manual page 16: 1cm from top-left */
.header {
  position: absolute;
  top: 1.72rem;
  left: 1.72rem;
  z-index: 10;
}

.header-logo {
  height: 1.72rem; /* 1cm */
  width: auto;
}

/* Content Area
 * CD Manual page 16: Content starts at 1.72cm horizontally
 * and at least 2.6cm vertically
 */
.content {
  flex: 1;
  padding: 4.5rem 3.44rem 4.5rem 3.44rem;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

/* Typography in Content */
.content :deep(h1) {
  font-size: 2.5rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.content :deep(h2) {
  font-size: 2rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 1.25rem;
  margin-top: 2rem;
  line-height: 1.2;
}

.content :deep(h3) {
  font-size: 1.5rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 1rem;
  margin-top: 1.5rem;
}

.content :deep(h4) {
  font-size: 1.25rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 0.75rem;
  margin-top: 1.25rem;
}

.content :deep(p) {
  font-size: 1.125rem;
  line-height: 1.6;
  margin-bottom: 1rem;
  color: #000;
}

.content :deep(ul), 
.content :deep(ol) {
  font-size: 1.125rem;
  line-height: 1.6;
  margin-left: 1.5rem;
  margin-bottom: 1rem;
}

.content :deep(li) {
  margin-bottom: 0.5rem;
}

.content :deep(strong) {
  font-weight: bold;
  color: #000;
}

.content :deep(a) {
  color: #009FE3; /* Himmelblau */
  text-decoration: none;
  transition: opacity 0.2s ease;
}

.content :deep(a:hover) {
  opacity: 0.8;
  text-decoration: underline;
}

.content :deep(code) {
  background: #DEF0FA; /* Hellblau */
  padding: 0.125rem 0.375rem;
  border-radius: 3px;
  font-family: 'Consolas', 'Monaco', monospace;
}

.content :deep(pre) {
  background: #09202C; /* Mitternachtsblau */
  color: white;
  padding: 1rem;
  border-radius: 4px;
  overflow-x: auto;
  margin: 1rem 0;
}

.content :deep(pre code) {
  background: transparent;
  color: white;
}

.content :deep(blockquote) {
  border-left: 4px solid #009FE3;
  padding-left: 1.5rem;
  margin: 1.5rem 0;
  font-style: italic;
  color: #09202C;
}

.content :deep(table) {
  width: 100%;
  border-collapse: collapse;
  margin: 1rem 0;
}

.content :deep(th),
.content :deep(td) {
  padding: 0.75rem;
  text-align: left;
  border-bottom: 1px solid #999;
}

.content :deep(th) {
  font-weight: bold;
  background: #DEF0FA;
}

/* Footer */
.footer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 0.75rem 3.44rem;
  background: white;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.875rem;
  color: #666;
  border-top: 1px solid #999;
  padding-top: 0.5rem;
}

.footer-left {
  font-weight: normal;
}

.footer-right {
  font-weight: normal;
}

.page-number {
  color: #000;
}

/* Responsive */
@media (max-width: 1024px) {
  .content {
    padding: 4rem 2rem 4rem 2rem;
  }
  
  .footer {
    padding: 1rem 2rem;
  }
}
</style>