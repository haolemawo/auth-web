<template>
  <div class="color-list">
    <div
      class="color-item"
      v-for="color in colors"
      v-dragging="{ item: color, list: colors, group: 'color', otherData: otherData }"
      :key="color.text"
    >{{color.text}}</div>

  </div>
</template>
<script>
export default {
  mounted() {
    this.$dragging.$on("dragged", ({ value }) => {
      console.log(value.item);
      console.log(value.list);
      console.log(value.otherData);
    });
    this.$dragging.$on("dragend", () => {});
  },

  data() {
    return {
      colors: [
        {
          text: "Aquamarine"
        },
        {
          text: "Hotpink"
        },
        {
          text: "Gold"
        },
        {
          text: "Crimson"
        },
        {
          text: "Blueviolet"
        },
        {
          text: "Lightblue"
        },
        {
          text: "Cornflowerblue"
        },
        {
          text: "Skyblue"
        },
        {
          text: "Burlywood"
        }
      ]
    };
  }
};
</script>
