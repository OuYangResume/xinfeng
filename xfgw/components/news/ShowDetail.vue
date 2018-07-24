<template>
<div>
    <!-- <div v-html="content"></div> -->
    <div v-html="parseData"></div>
</div>
</template>
<script>
export default {
    data () {
        return {
            content1: null
        }
    },
    computed: {
        parseData: function(){
            console.log(this.content)
            return this.content.data.content
        }
    },
  props: {
    content: {
      type: String
    }
  }
};
</script>