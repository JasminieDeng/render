<template>
  <div id="render">
    template
  </div>
</template>
<script>
import TemplateV1 from "./v1.js";
export default {
  name: "templateV",
  mounted() {
    const v1 = new TemplateV1().mounted(this.$el);
    v1.render(this.render(), {
      image: "https://img0.baidu.com/it/u=103721101,4076571305&fm=26&fmt=auto&gp=0.jpg",
      info: { showImage: true, showDate: false, name: "aaa" },
    });
    console.log(v1);
  },
  methods: {
    render() {
      return `<div class="newslist">
          <div class="img" v-if="info.showImage"><img src="{{image}}"/></div>
          <div class="date" v-if="info.showDate">{{info.name}}</div>
          <div class="img">{{info.name}}</div>
      </div>`;
    },
  },
};
</script>
