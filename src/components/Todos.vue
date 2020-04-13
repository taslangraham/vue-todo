<template>
  <div class="container">
    <div class="row" style="margin-top:80px;">
      <div class=".center-align col-8">
        <app-add-item :addItemFn="addItem"></app-add-item>
      </div>
      <!-- <hr /> -->
    </div>

    <div class="teal lighten-2">
      <div class="card-panel teal lighten-3 heading" v-if="items.length>0">
        <h6>Current Items</h6>
      </div>
    </div>

    <div class="items">
      <div v-for="(item,i) in items" :key="i">
        <todo :item="item" :todoId="i" @del-todo="deleteItem"></todo>
      </div>
    </div>
  </div>
</template>

<script>
import Todo from "./TodoItem";
import AddItem from "./AddItem";
export default {
  data() {
    return {
      items: []
    };
  },
  components: {
    todo: Todo,
    "app-add-item": AddItem
  },

  methods: {
    addItem(item) {
      this.items.unshift(item);
    },
    deleteItem(id) {
      this.items = this.items.filter((item, i) => {
        return i != id;
      });
    }
  }
};
</script>

<style lang="css" scoped>
</style>