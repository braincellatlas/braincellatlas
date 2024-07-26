<template>
  <div style="background:white;">
    <!-- <div class="wrap"> -->
    <!-- <component :is="component" :key="component.name" :atlasName="atlasName" /> -->
    <IndexComp />
    <div class="wrap">
    <div class="contact-wrap">
    <div class="mtit">
        <div class="t">Cite us</div>
        <div class="f">
          <p>Xinyue Chen#, Yin Huang#, Liangfeng Huang#, Ziliang Huang#, Zhao-Zhe Hao#, Lahong Xu, Nana Xu, Zhi Li, Yonggao Mou, Mingli Ye, Renke You, Xuegong Zhang, Sheng Liu*, Zhichao Miao*. A brain cell atlas integrating single-cell transcriptomes across human brain regions. <i>Nat Med</i> (2024). <a href="https://doi.org/10.1038/s41591-024-03150-z">https://doi.org/10.1038/s41591-024-03150-z</a>.</p>
        </div>
      </div>
    </div>
  </div>
    <div style="height: 30px"></div>
    <!-- </div> -->

  </div>
</template>
<script>
export default {
  name: "index",
  components: {
    AnatomyBrain: () => import("./components/AnatomyBrain.vue"),
    IndexComp: () => import("./components/IndexComp.vue"),
  },
  data () {
    return {
      atlasName: "",
      component: "IndexComp",
    };
  },
  watch: {
    $route (to, from) {
      console.log(to);
      if (to.query.atlasName && to.path == "/index") {
        this.component = "AnatomyBrain";
        const { atlasName } = to.query;
        this.atlasName = atlasName;
      } else if (!to.query.atlasName && to.path == "/index") {
        this.component = "IndexComp";
      }
    },
  },
  mounted () {
    if (this.$route.query.atlasName && this.$route.path == "/index") {
      this.component = "AnatomyBrain";
      const { atlasName } = this.$route.query;
      this.atlasName = atlasName;
    } else if (!this.$route.query.atlasName && this.$route.path == "/index") {
      this.component = "IndexComp";
    }
  },
};
</script>
<style lang="scss" scoped>
.contact-wrap {
  margin-top: 60px;
}
.mtit {
  .t {
    font-size: 24px;
    line-height: 62px;
  }
  .f p {
    padding-top: 0px;
  }
}
</style>