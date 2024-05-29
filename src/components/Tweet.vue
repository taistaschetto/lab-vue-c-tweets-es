<script setup>
import { defineProps } from "vue";
import { ref } from "vue";
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";

const props = defineProps({
  tweet: Object,
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :userData="tweet.user" />

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
