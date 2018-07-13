# VUE Path Breadcrumb 文件路径层级面包屑

> 效果：
> 返回上一级 | 全部文件 Mark Lopez > Timothy > Robinson > Mark Clark Cynthia > Jackson > John Wilson

```
//安装依赖
npm i -S vue-echarts-sedu
//运行项目
npm run dev
```

> 调用

```
main.js:   加入
  import seduPathBreadcrumb from 'vue-path-breadcrumb'

  Vue.use(seduPathBreadcrumb);

---

<template>
  <sedu-path-breadcrumb ref="seduPathBreadcrumb"
                        :callBack="getFileList" />
</template>

---
<script>
  mounted () {
    // 把根路径加入面包屑，对象是你刷新数据时要发送的json对象。
    this.$refs.seduPathBreadcrumb.addPath({key: 666})
  },
  methods: {
    // a链接的方法中也要把对象传入面包屑
    // 对象最少包含2个字段
    // {
    //    name:'目录名',    //面包屑上显示的目录名
    //    key:'234feewrwr'  //更新父组件文件列表需要的关键字
    // }
    updateTable (obj) {
      this.$refs.seduPathBreadcrumb.addPath(obj)
      this.getFileList(obj)
    },
  }
</script>
```
