<template>
  <div class="field">
    <label class="label" :for="label">{{ label }}</label>
    <div class="control">
      <input v-bind="$attrs"
          class="input" type="text" :name="name" :value="modelValue" :placeholder="label"
             @input="$emit('update:modelValue', $event.target.value)">
    </div>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: ''
    },
    modelValue: {
      type: [String, Number],
      default: ''
    }
  }
}
</script>