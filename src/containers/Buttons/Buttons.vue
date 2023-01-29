<template>
  <TextButtons />
  <ContainedButtons />
  <OutlinedButtons />
  <IconButtons />
</template>

<script>
import TextButtons from '@/containers/Buttons/TextButtons.vue';
import ContainedButtons from '@/containers/Buttons/ContainedButtons.vue';
import OutlinedButtons from '@/containers/Buttons/OutlinedButtons.vue';
import IconButtons from '@/containers/Buttons/IconButtons.vue';

export default {
  name: "Buttons",
  components: {
    TextButtons,
    ContainedButtons,
    OutlinedButtons,
    IconButtons
  }
}
</script>

<style scoped>

</style>