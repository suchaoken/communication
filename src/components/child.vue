<!--  第一种props＋$emit -->
<!--
<template>
  <div>
      我是子组件
    <div>{{ message }}</div>
    <button @click="change">弹</button>
  </div>
</template>

<script>
export default {
  props: ["message"],
  methods: {
    change: function () {
      this.$emit("clicker",'bye');
    },
  },
};
</script>
-->
<!-- ----------------------------------------------------------------------------- -->

<!-- 第二种 回调函数 -->
<!-- 
<template>
  <div>
    我是子组件
    <div>{{ message }}</div>
    <button @click="clicker">弹</button>
  </div>
</template>

<script>
export default {
  props: ["message", "clicker"],
};
</script>
-->
<!-- ----------------------------------------------------------------------------- -->

<!-- 第三种 $parent+$children $children在vue3中不存在 -->
<!-- 
<template>
  <div>
    我是子组件
    <div>{{ parentMessage }}</div>

  </div>
</template>

<script>
export default {

  computed: {
    parentMessage() {
      return this.$parent.message;
    },
  },
};
</script>
-->
<!-- ----------------------------------------------------------------------------- -->

<!-- 第四种 provide+inject  -->
<!--
<template>
  <div>
    我是子组件
    <div>{{msg }}</div>

  </div>
</template>

<script>
export default {
inject:['msg']
};
</script>
-->

<!-- ----------------------------------------------------------------------------- -->
