<template>
  <div>
    <!-- vue2 -->
    <input
      type="text"
      :value="value"
      @input="$emit(
        'input',
        $event.target.value
      )"
    >

    <!-- vue3 -->
    <input
      type="text"
      :value="modelValue"
      @input="$emit(
        'update:modelValue',
        $event.target.value
      )"
    >

  </div>
</template>

<script>
export default {
  name: 'VueModel',

  props: {
    value: {
      type: [String, Number],
      default: null
    },
    modelValue: {
      type: [String, Number],
      default: null
    }
  }
}
</script>
