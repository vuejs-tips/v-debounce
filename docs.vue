<template lang="html">
<div class="container col-4 col-xl-6 col-md-8 col-sm-10 col-xs-12">
  <h1 class="text-center">v-debounce</h1>
  <p class="text-center">
    Micro directive to delay input typing.
  </p>

  <p class="text-center">
    <code><pre>&lt;input v-model.lazy="sample" v-debounce="delay" /&gt;</pre></code>
  </p>
  <p>
    <input v-debounce="delay" v-model.lazy="sample" class="form-input input-lg" />
  </p>
  <p class="label label-primary">
    {{sample}}
  </p>

  <p>
    <label class="form-label">Delay</label>
    <input type="number" v-model.number="delay" class="form-input input-sm" />
  </p>

  <p class="text-center">
    <a class="btn" href="https://github.com/vuejs-tips/v-debounce">https://github.com/vuejs-tips/v-debounce</a>
  </p>
</div>
</template>

<script>

import debounce from './index'

export default {
  data () {
    return {
      sample: 'sample',
      delay: 500
    }
  },

  directives: {debounce}
}
</script>

<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/spectre.css/0.2.14/spectre.min.css');
</style>
