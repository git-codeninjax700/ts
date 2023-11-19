<template>
  <div>
    <button @click="handleEvent(1)">Event 1</button>
    <button @click="handleEvent(2)">Event 2</button>
    <button @click="handleEvent(3)">Event 3</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      eventIds: []
    };
  },
  methods: {
    handleEvent(eventId) {
      // Store the event ID in the data property
      this.eventIds.push(eventId);
      
      // Or emit the event ID to a parent component
      this.$emit('event-collected', eventId);
    }
  }
};
</script>
