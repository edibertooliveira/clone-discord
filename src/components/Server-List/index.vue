<template>
  <div class="container">
    <ServerButton isHome/>
    <div class="separetion"></div>
    <ServerButton :mentions="3"/>
    <ServerButton :mentions="20" hasNotification/>
    <ServerButton :mentions="5"/>
    <ServerButton hasNotification/>
    <ServerButton :mentions="5"/>
    <ServerButton :mentions="3"/>
    <ServerButton hasNotification/>
    <ServerButton v-for="servers in 10" :key="servers.id"/>
  </div>
</template>

<script>
  import ServerButton from "./ServerButton";

export default {
  components: {
    ServerButton
  }
}

</script>

<style scoped lang="scss">
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    grid-area: SL;
    background: var(--tertiary);
    padding: 11px 0;
    max-height: 100vh;
    overflow-y:scroll;
    &::-webkit-scrollbar{
      display: none;
    }
  }

  .separetion {
    width: 32px;
    margin-bottom: 8px;
    border-bottom: 2px solid var(--quaternary);
  }
</style>
