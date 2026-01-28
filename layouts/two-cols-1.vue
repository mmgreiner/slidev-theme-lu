<template>
  <div class="slidev-layout two-cols-layout">
    <!-- Logo -->
    <div class="header">
      <img src="/Logo_Kanton_Luzern_RGB.svg" alt="Kanton Luzern" class="header-logo" />
    </div>
    
    <!-- Two columns -->
    <div class="main-content">
      <div class="left-col">
        <slot name="left" />
      </div>
      
      <div class="right-col">
        <slot name="right" />
      </div>
    </div>
    
    <!-- Footer -->
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
.two-cols-layout {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background: white;
  color: #000;
}

.header {
  position: absolute;
  top: 1.72rem;
  left: 1.72rem;
  z-index: 10;
}

.header-logo {
  height: 1.72rem;
  width: auto;
}

.main-content {
  flex: 1;
  display: flex;
  gap: 3rem;
  padding: 4.5rem 3.44rem 4rem 3.44rem;
}

.left-col,
.right-col {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow-y: auto;
}

.left-col :deep(h1),
.right-col :deep(h1) {
  font-size: 2rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 1.5rem;
}

.left-col :deep(h2),
.right-col :deep(h2) {
  font-size: 1.5rem;
  font-weight: bold;
  color: #000;
  margin-bottom: 1.25rem;
}

.left-col :deep(p),
.right-col :deep(p) {
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.left-col :deep(ul),
.right-col :deep(ul) {
  font-size: 1rem;
  line-height: 1.6;
  margin-left: 1.5rem;
}

.left-col :deep(img),
.right-col :deep(img) {
  max-width: 100%;
  height: auto;
  border-radius: 4px;
}

.footer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 1rem 3.44rem;
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

.page-number {
  color: #000;
}

@media (max-width: 1024px) {
  .main-content {
    flex-direction: column;
    gap: 2rem;
  }
}
</style>