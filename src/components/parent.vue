<!-- 第一种 props＋$emit -->
<!--
<template>
  <div>
    <div>我是父组件</div>
    ------------------------------
    <child :message="message" @clicker="parentchange($event)"></child>
  </div>
</template>

<script>
import child from "./child.vue";
export default {
  components: {
    child,
  },
  data(){
    return{
      message:'zhangsan'
    }
  },
  methods:{
    parentchange:function($event){
      this.message = $event

    }
  }
};

</script>
-->
<!-- ----------------------------------------------------------------------------- -->

<!-- 第二种 回调函数 -->
<!--
<template>
  <div>
    <div>我是父组件</div>
    ------------------------------
    <child :message="message" :clicker="parentchange"></child>
  </div>
</template>

<script>
import child from "./child.vue";
export default {
  components: {
    child,
  },
  data(){
    return{
      message:'zhangsan'
    }
  },
  methods:{
    parentchange:function(){
      this.message = 'lisi'

    }
  }
};
</script>
-->
<!-- ----------------------------------------------------------------------------- -->

<!-- 第三种 $parent+$children  $children在vue3中不存在-->
<!--
<template>
  <div>
    <div>我是父组件</div>
    <div>{{msg}}</div>
    ------------------------------
    <child ></child>
  </div>
</template>
<script>
import child from "./child.vue";
export default {
  components: {
    child,
  },
  data() {
    return {
      msg: "wangwu",
    };
  },
};
</script>

-->
<!-- ----------------------------------------------------------------------------- -->

<!-- 第四种 provide+inject  -->
<!--
<template>
  <div>
    <div>我是父组件</div>
    ------------------------------
    <child></child>
  </div>
</template>
<script>
import child from "./child.vue";
export default {
  components: {
    child,
  },
  provide: {
    msg: "hello",
  },
};
</script>
 -->
<!-- ----------------------------------------------------------------------------- -->

