<template>
  <div class="sort">
    <div class="sort-head">
      <p class="sort-head-p" @click="gosearch"><span>畅想20</span></p>
    </div>
    <div class="sort-content">
      <div class="sort-left">
          <div class="sort-left-div" v-for="(item,index) in list" :key="index"><a href="#" @click="tab(index)" :class="{active:num==index}">{{item}}</a></div>
      </div>
      <div class="sort-right">
          <div class="sort-right-content" v-for="(item,index) in contentlist" :key="index" v-show="index==num">
              <div class="sort-right-content-headimg">
                <img :src="item.headimg" alt="">
              </div>
              <div class="sort-right-content-title">{{item.name}}</div>
              <div class="sort-right-content-box">
                  <div class="sort-right-content-img" v-for="(item,index) in item.contentimg" :key="index" @click="gocart(index)">
                      <img :src="item.img" alt="">
                      <p style="fontSize:13px;color:#666">{{item.title}}</p>
                  </div>
              </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
      return{
        num:0,
        list:["新品","华为手机","荣耀手机","笔记本","平板","智能穿戴&VR","智能屏","智能家居","耳机音箱","专属配件","通用配件","生态产品","增值服务","智能计算"],
        contentlist:[
        {
            "headimg":require("../../assets/c11.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c11.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c11.jpg"),
                  "title":"HUAWEI P40 Pro+"
                },
                {
                  "img":require("../../assets/c11.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c11.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c21.jpg"),
            "name":"HUAWEI P系列",
            "contentimg":[
                {
                  "img":require("../../assets/c21.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c21.jpg"),
                  "title":"HUAWEI P40 Pro+"
                },
                {
                  "img":require("../../assets/c21.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c21.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"荣耀 V系列",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"笔记本电脑",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        },
        {
            "headimg":require("../../assets/c23.jpg"),
            "name":"手机",
            "contentimg":[
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 5G"
                },
                {
                  "img":require("../../assets/c23.jpg"),
                  "title":"HUAWEI P40 Pro+"
                }
            ]
        }
    ]
      }
    },

    methods:{
      tab(index){
        console.log(index);
        this.num = index
      },
      gocart(index){
        console.log(index);
      },
      gosearch(){
        this.$router.push('/search')
      }
    }
};
</script>

<style scoped>
.sort {
  width: 100%;
  height: 100%;
}

.sort-head {
  width: 100%;
  height: 8%;
   /* padding-top: 5px; */
   text-align: center;
}

.sort-head-p {
  margin-left: 20px;
  width: 80%;
  height: 70%;
  background: #f5f5f5;
  border-radius: 30px;
  position: relative;
  top: 3px;
}

.sort-head-p span{
    color: rgb(194, 190, 190);
  font-size: 14px;
  line-height: 33px;
  margin-left: 10px;
}

.sort-content {
  width: 100%;
  height: 92%;
  display: flex;
  overflow: auto;
}

.sort-left{
    width: 30%;
    height: 100%;
    overflow: auto;
}

.sort-left-div{
    width: 100%;
    height: 51px;
}

.sort-left-div a{
    display: inline-block;
    width: 80%;
    margin-left: 15%;
    font-size: 15px;
    color: #000;
    padding-top: 5px;
}

.active{
  border-right: 3px solid #e01d20;
}

.sort-right{
    width: 70%;
    height: 100%;   
    overflow: auto;
}

.sort-right-content{
    width: 100%;
    height: 100%;
    margin: 0 auto;
}

.sort-right-content-headimg,.sort-right-content-headimg>img{
  width: 100%;
  height: 80px;
}

.sort-right-content-title{
  width: 100%;
  height: 46px;
  text-align: center;
  line-height: 46px;
}

.sort-right-content-box{
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.sort-right-content-img{
  width: 33.3%;
  height: 124px;
  text-align: center;
}

.sort-right-content-img>img{
  width: 55px;
  height: 55px;
  margin-top: 20px;
}
</style>