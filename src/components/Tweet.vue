<script setup>
import { defineProps } from 'vue';
import { ref } from 'vue';
import ProfileImage from './ProfileImage.vue';

const props = defineProps({
  tweet: Object,
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image"/>
  
    <div class="body">
      <div class="top">
        <span class="user">
          <span class="name">{{ tweet.user.name }}</span>
          <span class="handle">@{{ tweet.user.handle }}</span>
        </span>
  
        <span class="timestamp">{{ tweet.timestamp }}</span>
      </div>
  
      <p class="message">{{ tweet.message }}</p>
  
      <div class="actions">
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>
  
    <i class="fas fa-ellipsis-h"></i>
  </div>
  </template>

<style scoped>
a {
  color: #42b983;
}
</style>
