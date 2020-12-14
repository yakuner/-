<template>
 
    <div>
    <Header />
    <div class="container">
     <Add :addComment="addComment"/>
     <ShowList :comments="comments" :deleteComment="deleteComment"/>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header'
import Add from '@/components/Add'
import ShowList from '@/components/ShowList'
export default {
  name: '',
  // 数据定义在哪里,要看哪个组件使用数据,或者哪几个组件使用这个数据,
  // 如果是只有一个使用那么就定义在使用这个数据的组件中,如果好几个组件都要用,
  // 那么交给他们共同的父组件,使用包括增删改查
  data(){
    return{
      comments:[
        {id:1,userName:'宋江',centent:'这还真不赖'},
        {id:2,userName:'武松',centent:'这还真挺好'},
        {id:3,userName:'林冲',centent:'vue不错'},
        {id:4,userName:'卢俊义',centent:'这还还可'}
      ],
    }
  },
  components:{
    Header,Add,ShowList
  },
  methods:{
    addComment(comment){
      if(comment){
         this.comments.unshift(comment)
      }
    },
    deleteComment(index){
      this.comments.splice(index,1)
    }
  }
}
</script>

<style scoped>

</style>
