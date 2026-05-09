<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Motivation from './sections/Motivation.vue'
import Framework from './sections/Framework.vue'
import MainResults from './sections/MainResults.vue'
import VisualExp from './sections/VisualExp.vue'
import FurtherAnalysis from './sections/FurtherAnalysis.vue'
import CaseStudy from './sections/CaseStudy.vue'
import BibTeX from './sections/BibTeX.vue'

export default {
  components: {
    Title,
    Abstract,
    Motivation,
    Framework,
    MainResults,
    VisualExp,
    FurtherAnalysis,
    CaseStudy,
    BibTeX,
  }
}
</script>

<template>
  <Title/>
  <VisualExp/>
  <Abstract/>
  <Motivation/>
  <Framework/>
  <MainResults/>
  <FurtherAnalysis/>
  <CaseStudy/>
  <BibTeX/>
</template>
