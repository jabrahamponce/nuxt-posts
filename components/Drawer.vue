<template>
  <div>
    <c-button ref="btnRef" @click="isOpen = true">Menu</c-button>
    <c-drawer
      :is-open="isOpen"
      placement="right"
      :on-close="close"
      :initial-focus-ref="() => $refs.inputInsideModal"
    >
      <c-drawer-overlay />
      <c-drawer-content>
        <c-drawer-close-button />
        <c-drawer-header>MENU</c-drawer-header>

        <c-drawer-body>
          <ul>
            <li>Home</li>
            <li>Posts</li>
            <li>About</li>
            <li>Contact</li>
          </ul>
        </c-drawer-body>

        <!-- <c-drawer-footer>
          <c-button variant="outline" mr="3" @click="isOpen = false">
            Cancel
          </c-button>
          <c-button variant-color="blue">Save</c-button>
        </c-drawer-footer> -->
      </c-drawer-content>
    </c-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    close() {
      this.isOpen = false
    },
  },
}
</script>
