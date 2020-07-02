<template>
  <div>
    <order-header title="订单列表">
      <template v-slot:tip>
        <span>谨防钓鱼链接、</span>
      </template>
    </order-header>orderList
  </div>
</template>
<script>
import OrderHeader from "./../components/OrderHeader";
export default {
  name: "order-list",

  components: {
    OrderHeader,
  }
};
</script>