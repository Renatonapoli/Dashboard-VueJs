<template>
  <teleport to='body'>
    <div
    v-if="state.isActive"
    class="fixed top-0 left-0 z-50 items-center justify-center w-full h-full bg-black bg-opacity-50"
    @click="handleModalToogle({ status: false })"
    >
      <div class="fixed mx-10"
      >
        <div class=" flex flex-col overflow-hidden bg-white rounded-lg animate__animate animate__fadeInDown animate__faster">
          <div class="flex flex-col px-12 py-10 bg-white">
            <component :is="state.component" />
          </div>
        </div>

      </div>
    </div>
  </<teleport>
</template>

<script>
export default {
  setup() {
    const state = reactive({
      isActive: false,
      component: {},
      props: {},
      width: DEFAULT_WIDTH
    })

    function handleModalToogle ({ status}) {

    }
    return {
      state
    }
  }
}
</script>
