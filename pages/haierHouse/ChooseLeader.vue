<template>
  <view>
    <b-checkbox-list title="选择一站筑家负责人" :list="list" :checkedId.sync="checkedId" :handleChange="change"></b-checkbox-list>
  </view>
</template>

<script>
  import BCheckboxList from "../../components/common/BCheckboxList";

  export default {
    name: "ChooseLeader",
    components: {
      BCheckboxList
    },
    data() {
      return {
        checkedId: [],
        list: [{
            id: '1',
            val: '张亮'
          },
          {
            id: '2',
            val: '刘宏伟'
          },
          {
            id: '3',
            val: '孙大壮'
          },
          {
            id: '4',
            val: '王志欢'
          },
          {
            id: '5',
            val: '孙代'
          }
        ]
      };
    },
    methods: {
      change() {
        uni.navigateTo({
          url: '/pages/haierHouse/HaierHouseApply'
        });
      }
    }
  }
</script>

<style scoped>

</style>
