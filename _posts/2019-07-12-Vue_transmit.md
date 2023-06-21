---
layout: post
title: Vue 如何传值
img: vue.jpg
date: 2019-07-22
tag: 技术
category:  技术

---
### **子组件获取父组件的变量**

> 父：

```
<template>
  <div>
      <tbar :aa="aa"></tbar>
  </div>
</template>

<script>
export default {
    data () {
         return {
              aa:'-1',
         },
    }
}
</script>

```

> 子：

```
<template>
  <div>
     {{aa}}     //此处是显示从父获取到的变量 aa
  </div>
</template

<script>
export default{
   props:['aa'],
}
</script>
```


### **父组件获取子组件的变量**
- 在引用的子组件添加属性：ref = "tbar"，指向子组件对象，
- 然后通过 this.$refs.tbar.变量名，读取子组件的变量

> 父：

```
<template>
   <div>
       <tbar ref="tbar"></tbar>
    </div>
</template>

<script>
export default {
    methods: {
         getChild(){
              return this.$refs.tbar.bb;
        },
}
</script>
```

> 子：

```
<template>
   <div> 
    </div>
</template>
<script>
   export default{
         data () {
            return {
                bb:'我是子组件'
             }
         }
     }
</script>
```





