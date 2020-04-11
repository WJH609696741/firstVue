<template>
  <div class="first">
    <h1>计数器</h1>
    <div class="input-num">
        <button v-on:click = "sub">
            -
        </button>
        <span>{{ num }}</span>
        <button v-on:click = "add">
            +
        </button>
    </div>
  </div>
</template>

<script>
export default {
    data: () => {
        return {
           num: 1
        }
    },
    methods:{
        add(){
            // console.log('add');
            if(this.num<10){
                this.num++;
            }
            else{
                alert('别点了 最大了');
            }
        },
        sub:function(){
            // console.log('sub');
            if(this.num>0){
                this.num--;
            }
            else{
                alert('别点了 最小了');
            }
        }
    }
}
</script>

<style lang="less">
    * {
        margin: 0;
        padding: 0;
    }

    .input-num {
        width: 300px;
        margin:150px auto;
        text-align: center;
        border: 1px solid rgb(165, 165, 165);
        padding: 20px 0px;
    }
    .input-num button {
        /* border: 1px solid rgb(165, 165, 165); */
        width: 50px;
        height: 30px;
        background: #59dcd6;
        border-radius: 5px;
    }
    .input-num span {
        display: inline-block;
        width: 40px;
        height: 30px;
        /* border: 1px solid rgb(165, 165, 165); */
    }

</style>>
