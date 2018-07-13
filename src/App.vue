<template>
  <div>
    <!-- 语言切换 -->
    <sedu-path-breadcrumb ref="seduPathBreadcrumb"
                          :callBack="getFileList"></sedu-path-breadcrumb>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      targetPath: null,
    };
  },
  created() {},
  mounted () {
    // 把根路径加入面包屑
    this.$refs.seduPathBreadcrumb.addPath({key: 666})
  },
  methods:{
    getFileList () {
    },
  }
};
</script>

