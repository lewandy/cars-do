<template>
  <ion-list>
    <MessageListItem
      v-for="message in messages"
      :key="message.id"
      :message="message"
    />
  </ion-list>
</template>

<script>
import { IonList } from "@ionic/vue";
import { getMessages } from "@/data/messages";
import MessageListItem from "./MessageListItem.vue";

export default {
  name: "CarListContainer",
  data() {
    return {
      messages: getMessages(),
    };
  },
  components: {
    IonList,
    MessageListItem,
  },
};
</script>

<style>
</style>