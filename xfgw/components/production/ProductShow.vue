<template>
    <Card style="margin-top: 20px;margin-left: 50px;">
        <div style="text-align:center">
            <img style="width: 400px; height: 280px;" class="listImg" :src="imgSrc">
            <h3>{{imgTitle}}</h3>
        </div>
    </Card>
</template>
<script>
    export default {
        props: {
            imgSrc: {
                type: String
            },
            imgTitle: {
                type: String
            }
        }
    }
</script>
<style scoped>
.listImg{
    width: 400px;
    height: 280px;
}
</style>

