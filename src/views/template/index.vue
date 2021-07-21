<template>
	<div id="render">
		template
	</div>
</template>
<script>
	import TemplateV1 from './v1.js'
	export default {
		name: 'templateV',
		mounted() {
			const v1 = new TemplateV1().mounted(this.$el)
			v1.render(
				this.render() , {
					"newslist": [{
						"image": "http://dingyue.ws.126.net/2021/0201/b63f2e50j00qntwfh0020c000hs00npg.jpg?imageView&thumbnail=140y88&quality=85",
						"passtime": "2021-02-02 10:00:51",
						"path": "https://www.163.com/dy/article/G1OBC8LO0514BCL4.html",
						"title": "被指偷拿半卷卫生纸 63岁女洗碗工服药自杀 酒店回应",
					}]
				}
			)
			console.log(v1)
		},
		methods:{
			render() {
			    return `
			        <div class="newslist">
			            <div class="news-item" for="item in newslist">
			                <div class="img"><img src="{{item.image}}"/></div>
			                <div class="title">{{item.title}}</div>
			            </div>
			        </div>
			    `;
			  },
		}

	}
</script>
