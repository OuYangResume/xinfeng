<template>
<!-- <a href="/news/NewsDetail"> -->
    <div class="msg" @click="toNewsDetail(contentId)">
        <div class="msgListTitle">
            <span>{{title}}</span>
            <span>{{time}}</span>
        </div>
        <div class="msgListContent">
            <!-- <span> -->
                <div >
                    {{digest}}
                </div>
            <!-- </span> -->
        </div>
    </div>
<!-- </a> -->
</template>
<script>
import axios from "axios";

export default {
    data () {
        return {
            contentIdS: null
        }
    },
    props: {
        contentId: {
            type: String
        },
        title: {
            type: String
        },
        time: {
            type: String
        },
        digest: {
            type: String
        }
    },
    methods: {
        toNewsDetail (contentId) {
            this.$router.push(`/news/${contentId}`)
        }
    }
}
</script>
<style scoped>
.msg{
    padding: 30px 0;
    border-bottom: 1px dashed #ccc;
    margin-bottom: 20px;
}
.msgListTitle{
    margin: 15px 0;
    display: flex;
    justify-content: space-between;
    font-size: 18px;
    color: #333;
    font-weight: bold;
}
.msgListTitle > span:nth-child(1){
    max-width: 400px;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
}
.msgListContent{
    font-size: 14px;
    color: #666;
}
.msgListContent > div {
  position: relative;
  line-height: 24px;
  /* 3 times the line-height to show 3 lines */
  height: 42px;
  overflow: hidden;
}
.msgListContent > div::after {
  content: "...";
  font-weight: bold;
  position: absolute;
  bottom: 0;
  right: 0;
  padding: 0 20px 1px 45px;
  background: url(http://css88.b0.upaiyun.com/css88/2014/09/ellipsis_bg.png)
    repeat-y;
}
</style>
