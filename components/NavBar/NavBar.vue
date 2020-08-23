<style scoped src="./style/index.scss"  lang="scss"></style>
<template>
  <div class="footer">
    <div v-for="(item,index) of items" :key="index">
      <NuxtLink :to="{path:item.path}" >{{item.name}}</NuxtLink>
    </div>
  </div>
</template>

<script>
    import Vue from 'vue'
    export default {
        name:"NavBar",
        data() {
            return {
                items:[
                    {
                        name:"发现",
                        path:"/",
                        cls:"find",
                    },
                    {
                        name:"视频",
                        path:"/video",
                        cls:"video",
                    },
                    {
                        name:"我的",
                        path:"myPage",
                        cls:"mys"
                    },{
                        name:"朋友",
                        path:'friendPage',
                        cls:"friend"

                    },{
                        name:"账号",
                        path:"accountPage",
                        cls:"accouunt",

                    }
                ]
            }
        },
        props:{
        },

        methods: {
            clickBar:function(){
                this.$router.push('/'+this.page)
            }
        }
    }


</script>
