<script lang="ts" setup>
const links = {
  Nerfies: 'https://github.com/nerfies/nerfies.github.io',
  Vue: 'https://vuejs.org/',
  Vite: 'https://vitejs.dev/',
  ElementPlus: 'https://element-plus.org/',
  template: 'https://github.com/JunyaoHu/academic-project-page-template-vue',
}
</script>

<template>
  <div class="bg">
    <el-watermark :content="['Micro-Defects expose Macro-Fakes']" :gap="['60','0']" :z-index="0">
      <el-row justify="center">
        <p class="footer">
          Page template inspired by
          <a :href="links.Nerfies">Nerfies</a> and
          <a :href="links.template">academic-project-page-template-vue</a>,<br/>
          powered by
          <a :href="links.Vue">Vue</a>,
          <a :href="links.Vite">Vite</a>, and
          <a :href="links.ElementPlus">Element Plus</a>.
        </p>
      </el-row>
    </el-watermark>
  </div>
</template>

<style scoped>
.bg {
  background-color: rgb(235, 235, 235);
}

.footer {
  text-align: center;
  margin: 20px;
  z-index: 1;
}
</style>
