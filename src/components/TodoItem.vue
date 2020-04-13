<template>
  <div class="item" :class="{completed:item.isCompleted}" @dblclick="setToComplete">
    <h4>{{item.title}}</h4>
    <button class="waves-effect waves-light btn" @click="$emit('del-todo',todoId)">X</button>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      required: true,
      type: Object
    },
    todoId: {
      required: true,
      type: Number
    }
  },
  methods: {
    setToComplete() {
      this.item.isCompleted = !this.item.isCompleted;
    }
  }
};
</script>

<style lang="css" scoped>
.item {
  background: #e53935;

  user-select: none;
}
:hover .item {
  cursor: pointer;
}

.completed {
  background: #a7ffeb;
}
</style>
