<template>
  <div>
    <li class="list-group-item">
        <div class="handle">
            <a href="javascript:;" @click="deletecomment">删除</a>
        </div>
        <p class="user"><span>{{comment.userName}}</span><span>说:</span></p>
        <p class="centence">{{comment.centent}}</p>
    </li>
  </div>
</template>

<script>
export default {
  name: '',
  props:['comment','deleteComment'],
  methods:{
    // 设置删除
    deletecomment(){
      this.deleteComment(this.index)
    }
  }
}
</script>

<style scoped>
.handle {
  width: 40px;
  border: 1px solid #ccc;
  background: #fff;
  position: absolute;
  right: 10px;
  top: 1px;
  text-align: center;
}

.handle a {
  display: block;
  text-decoration: none;
}

.list-group-item .centence {
  padding: 0px 50px;
}

.user {
  font-size: 22px;
}
</style>
