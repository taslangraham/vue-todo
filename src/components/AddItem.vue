<template>
  <div>
    <input type="text" placeholder="Item Name" v-model="title" />
    <button
      :class="{disabled:shouldBeActive()}"
      class="btn-floating btn-large waves-effect waves-light red"
      @click="addItemFn(addItem())"
    >
      <i class="material-icons">add</i>
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "",
      item: function() {
        this.isCompleted = false;
        this.title = "";
      }
    };
  },
  props: {
    addItemFn: {
      type: Function,
      required: true
    }
  },
  methods: {
    shouldBeActive() {
      return this.title.trim() === "" ? true : false;
    },
    addItem() {
      let newItem = new this.item();
      newItem.isCompleted = false;
      newItem.title = this.title;

      this.title = "";
      return newItem;
    }
  }
};
</script>