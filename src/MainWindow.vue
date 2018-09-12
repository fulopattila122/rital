<template>
  <Window title="Tasklists :: Rital" width="640" height="480" margined v-on:close="exit">
    <Box padded>
      
    <Box horizontal padded>
        <TextInput v-model="newtask" stretchy></TextInput>
        <Button :enabled="!!newtask">Add Task</Button>
      </Box>

      <Separator horizontal/>

      <Checkbox v-model="checkboxState" checked>Feed the cat</Checkbox>
      <Checkbox v-model="checkboxState">Mind the gap between the train and the platform</Checkbox>

    </Box>
  </Window>
</template>

<script>
export default {
  methods: {
    exit() {
      this.$exit();
    }
  }
};
</script>
