<script setup>
import FigureSection from './FigureSection.vue'
</script>

<template>
  <FigureSection
    title="Main Results"
    src="resources/main_table.png"
    alt="Detection performance on ImageNet"
  >
    <template #caption>
      <b>State-of-the-art on ImageNet across 9 generators.</b><br>
      Diffusion (ADM, ADMG, LDM, DiT), GANs (BigGAN, GigaGAN, StyleGAN-XL) and transformers
      (RQ-Transformer, Mask GIT). MDMF achieves the best average <b>AUROC&nbsp;95.65 / AP&nbsp;97.07</b>.
    </template>
  </FigureSection>
</template>
