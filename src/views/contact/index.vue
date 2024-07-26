<template>
  <div class="wrap">
    <div class="contact-wrap">
      <teamItem :data="lists" type="m" />
      <div class="f">
          <p>For any inquiries or concerns regarding the database, please reach out to us.</p>
        </div>
      <el-divider></el-divider>
      <div class="mtit">
        <div class="t">Reference</div>
        <div class="f">
          <p>Xinyue Chen#, Yin Huang#, Liangfeng Huang#, Ziliang Huang#, Zhao-Zhe Hao#, Lahong Xu, Nana Xu, Zhi Li, Yonggao Mou, Mingli Ye, Renke You, Xuegong Zhang, Sheng Liu*, Zhichao Miao*. A brain cell atlas integrating single-cell transcriptomes across human brain regions. <i>Nat Med</i> (2024). <a href="https://doi.org/10.1038/s41591-024-03150-z">https://doi.org/10.1038/s41591-024-03150-z</a>.</p>
        </div>
      </div>
      <el-divider></el-divider>
      <div class="mtit">
        <div class="t">Acknowledgements</div>
        <div class="f">
          <p>We thank Yifan Yang and Jie Tao for the data collection. We thank the authors of related datasets who kindly provided metadata of their studies.</p>
        </div>
      </div>
    </div>
    <div style="height: 30px"></div>
  </div>
</template>
<script>
export default {
  components: {
    teamItem: () => import("./components/teamItem.vue"),
  },
  data () {
    return {
      lists: [{
        name: "Xinyue Chen",
        img: require("@/assets/img/xiaoxiao.png"),
        desc: "PhD Candidate",
        email: "chen_xinyue@gzlab.ac.cn"
      }, {
        name: "Ziliang Huang",
        img: require("@/assets/img/xiaoxiao.png"),
        desc: "Research Assistant",
        email: "huang_ziliang@gzlab.ac.cn"
      // }, {
      //   name: "Dr Yin Huang",
      //   img: require("@/assets/img/xiaoxiao.png"),
      //   desc: "Postdoc",
      //   email: "huang_yin@gzlab.ac.cn"
      // }, {
      //   name: "Dr Lahong Xu",
      //   img: require("@/assets/img/xiaoxiao.png"),
      //   desc: "Postdoc",
      //   email: "xu_lahong@gzlab.ac.cn"
      // }, {
      //   name: "Prof Zhichao Miao",
      //   img: require("@/assets/img/xiaoxiao.png"),
      //   desc: "Principle Investigator",
      //   email: "miao_zhichao@gzlab.ac.cn"
      }],
    };
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
    padding-top: 22px;
  }
}
</style>
