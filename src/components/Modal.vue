<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-header">
            <slot name="header">Update Data</slot>
          </div>

          <div class="modal-body">
            <slot name="body">default body</slot>
          </div>

          <div class="modal-footer">
            <slot name="footer">
              <button class="modal-default-button btn btn-warning" @click="$emit('close')">Close</button>
              <button class="modal-default-button btn btn-success" @click="$emit('save')">Save</button>
            </slot>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "modal",
};
</script>
<style scoped>
.modal-container{
      position: fixed;
    box-shadow: rgb(0 0 0 / 25%) 0px 54px 55px, rgb(0 0 0 / 12%) 0px -12px 30px, rgb(0 0 0 / 12%) 0px 4px 6px, rgb(0 0 0 / 17%) 0px 12px 13px, rgb(0 0 0 / 9%) 0px -3px 5px;
    top: 0;
    left: 50%;
    right: 0;
    bottom: 0;
    z-index: 999;
    background: #9b2b2b;
    width: 50%;
    height: 50vh;
    transform: translate(-50%,50%);
    overflow: hidden;
}
</style>