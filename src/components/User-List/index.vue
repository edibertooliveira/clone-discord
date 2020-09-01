<template>
  <div class="userList">
    <div class="role">Disponivel - 2</div>
    <UserRow nickName="Ediberto Oliveira" />
    <UserRow nickName="MecBOT" isBot/>
    <div class="role">Indisponivel - 18</div>
    <UserRow nickName="Fulano de tal" v-for="user in 20" :key="user.id"/>
  </div>
</template>

<script>
import UserRow from  './UserRow';
export default {
  components: {
    UserRow,
  },
};
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
  .role {
    margin-top: 20px;
    color: var(--grey);
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
  }
</style>
