<template>
  <div>
    <div class="alert " :class="mode" role="alert">
        <slot></slot>
    </div>
            
  </div>
</template>

<script>
export default {
  name: 'Alert',
  props: [
    'mode'
  ],
  
}
</script>


<style scoped lang="scss">
.primary {
    color: #fff;
    background-color: #084298;
    border-color: #084298;
}
.success {
    color: #fff;
    background-color: #42b983;
    border-color: #42b983;
}
.danger {
    color: #fff;
    background-color: #6e194c94;
    border-color: #6e194c94;
}


.alert {
    position: relative;
    padding: 1rem 1rem;
    margin-bottom: 1rem;
    border: 1px solid transparent;
    border-radius: .25rem;
}
</style> 


