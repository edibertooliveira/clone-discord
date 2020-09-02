<template>
  <div class="ServerButton" :class="{'ServerButton-isHome':isHome,'ServerButton-hasNotification': hasNotification}">
    <!-- <img src="../../../dist/discord.svg" alt="discord" v-if="isHome"> -->
    <div class="mentions" v-if="mentions">{{mentions}}</div>
  </div>
</template>

<script>
export default {
  props: {
    selected: Boolean,
    isHome: Boolean,
    hasNotification: Boolean,
    mentions: Number,

  }
}
</script>

<style lang="scss" scoped>
  .ServerButton {
    display: flex;
    flex-shrink: 0;
    align-items: center;
    justify-content: center;
    width: 48px;
    height: 48px;
    margin-bottom: 8px;
    background: var(--primary);
    cursor: pointer;
    position: relative;
    border-radius: 50%;
    transition: 0.2s;
      &:hover,
      &.active {
      background: var(--discord);
      border-radius: 25%;
    }

    img {
    width: 24px;
    color: var(--white);

  }

  .mentions{
    background: var(--notification);
    width: auto;
    height: 24px;
    padding: 0 4px;
    position: absolute;
    bottom: -4px;
    right: -4px;
    border-radius: 12px;
    text-align: center;
    font-size: 13px;
    font-weight: bold;
    color: var(--white);
    border: solid 4px var(--quaternary);

  }

  }



  .ServerButton-hasNotification {
    &::before{
      content: '';
      width: 9px;
      height: 9px;
      background: var(--white);
      position: absolute;
      left: -17px;
      top: calc(50% - 4.5px);
      border-radius: 50%;
      display: block;

    }
  }

  .ServerButton-isHome {
    background: var(--link);
    &.active,
    &:hover {
      border-radius: 16px;
      background-color: var(--link);


    }
  }
</style>
