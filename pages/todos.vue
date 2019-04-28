<template>
<div>
  <ul>
    <li v-for="todo in todos">
      <input type="checkbox" :checked="todo.done" @change="toggle(todo)">
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
    </li>
    <li><input placeholder="What needs to be done?" @keyup.enter="addTodo"></li>

      <v-btn
                :block=true
                :large=true
                @click="clickHtml"
                color="grey darken-3 white--text">
                <span><i class="far fa-comment-dots"></i> はなす</span>
                </v-btn><v-btn
                :block=true
                :large=true
                @click="clickCSS"
                color="grey darken-3 white--text">
                <span><i class="far fa-comment-dots"></i> はなす</span>
                </v-btn>
    
  </ul>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  computed: {
    todos () { return this.$store.state.todos.list }
  },
  methods: {
    addTodo (e) {
      this.$store.commit('todos/add', e.target.value)
      e.target.value = ''
    },
    clickHtml(){
      this.$store.commit('comment/change', this.$store.state.comment.skillList.html)
    },
    clickCSS(){
      this.$store.commit('comment/change', this.$store.state.comment.skillList.css)
    },
    ...mapMutations({
      toggle: 'todos/toggle'
    })
  }
}
</script>

<style>
.done {
  text-decoration: line-through;
}
</style>