<template>
  <div class="userList">
    <div class="offline"></div>
    <div class="online"></div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .userList {
    display: flex;
    flex-direction: column;
    background: var(--secondary);
    grid-area: UL;
    padding: 3px 6px 10px 16px;
    max-height: calc(100vh - 46px);
    overflow-y: scroll;

  &::-webkit-scrollbar {
    width: 8px;
  }
  &::-webkit-scrollbar-thumb {
    background: var(--tertiary);
    border-radius: 4px;
  }

  &::-webkit-scrollbar-track {
    background: var(--secondary);
  }

  }
</style>
