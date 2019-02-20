<template>
  <nav class="nav-container">
    <ul>
      <li v-for="(topic, index) in topics" :key="index" :class="activeTopic === topic.value && 'active'">
        <a @click="setNewTopic(topic.value)">
        {{ topic.name }}
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
  export default {
    name: 'Nav',
    props: {
      activeTopic: {
        type: String
      },
      changeTopic: {
        type: Function
      }
    },
    data() {
      return {
        topics: [
          {
            name: 'Cupo trans',
            value: 'cupo-trans'
          },
          {
            name: 'Aborto legal',
            value: 'aborto-legal'
          },
          {
            name: 'ESI',
            value: 'esi'
          }
        ]
      }
    },
    methods: {
    setNewTopic: function(newTopic) {
      return this.changeTopic(newTopic)
    }
  }
  }
</script>

<style scoped>
  nav {
    margin-bottom: 40px;
  }
  ul {
    display: flex;
    justify-content: space-around;
    list-style: none;
  }
  li {
    cursor: pointer;
    padding: 0 10px 10px;
  }
  li:hover {
    font-weight: bold;
  }
  li.active {
    font-weight: bold;
    border-bottom: 2px solid #f38eb0;
  }
</style>