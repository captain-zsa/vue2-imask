<template>
  <div>
    <imask-input
      v-model="numberModel"
      :mask="Number"
      radix="."
      :unmask="true"
      @accept="onAccept"
      placeholder='Enter number here'
    />
  </div>
</template>

<script>
import { IMaskComponent } from 'vue-imask';
export default {
  name: 'IndexPage',

  data () {
    return {
      numberModel: '',
    }
  },
  components: {
    'imask-input': IMaskComponent
  },
  methods: {
    onAccept (value) {
      console.log(value);
    }
  }
}
</script>
