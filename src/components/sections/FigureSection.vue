<script setup>
defineProps({
  title: { type: String, required: true },
  src: { type: String, required: true },
  alt: { type: String, default: '' },
  span: { type: Object, default: () => ({ xs: 24, sm: 20, md: 16, lg: 12, xl: 12 }) },
})
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">{{ title }}</h1>
    </el-row>

    <el-row justify="center">
      <el-col :xs="span.xs" :sm="span.sm" :md="span.md" :lg="span.lg" :xl="span.xl">
        <el-image :src="src" :alt="alt" fit="contain" class="figure" lazy />
        <p class="caption"><slot name="caption" /></p>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.section-title {
  margin: 18px 0 8px;
}

.figure {
  display: block;
  width: 100%;
  margin: 12px auto 0;
}

.caption {
  font-size: 15px;
  line-height: 1.6;
  color: #444;
  text-align: center;
  margin: 14px 8px 8px;
}

.caption :deep(b) {
  color: #2c7a7b;
}
</style>
