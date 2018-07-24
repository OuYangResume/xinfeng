<template>
    <div>
        <div class="head">
            <TitleMsgShow title="新闻动态" titleEN="NEWS CENTER" titleBackground="123"></TitleMsgShow>
        </div>
        <div class="contentBigBox">
            <div class="contentBox">
                <ShowDetail :content="contents"></ShowDetail>
            </div>
        </div>
    </div>

</template>
<script>
    import axios from 'axios'
    import TitleMsgShow from '../../components/common/TitleMsgShow.vue'
    import Content from '../../components/news/Content.vue'
    import ShowDetail from '../../components/news/ShowDetail.vue'
    import NewsShow from '../../components/mainpage/NewsShow.vue'

    export default {
        props: {
            content: {
                type: String
            }
        },
        data() {
            return {

            }
        },
        components: {
            TitleMsgShow,
            Content,
            NewsShow,
            ShowDetail
        },
        async asyncData ({ params, error }) {
            console.log(params)
            const contents = await axios.get(`http://192.168.30.208:9000/XFGD/getContent?contentId=${params.contentId}`)

            return {
                contents,
            }
        },
    }
</script>
<style scoped>
.head {
  width: 100%;
  height: 300px;
  background-color: aqua;
  background-image: url("~/assets/img/linkme/联系我们.png");
  background-size: 100% 300px;
  margin-top: 100px;
}
.contentBigBox{
    display: flex;
    justify-content: center;
}
.contentBox{
  width: 1250px;
}
</style>


