<template>
  <div class="container">
    <div class="category">
      <div class="">Canais de texto</div>
      <div class="category-icon">
        <AddCategoryIcon :size="21"/>
      </div>
    </div>
    <ChannelButton channelName="Bem-Vindo"/>
    <ChannelButton channelName="REGRAS"/>
    <ChannelButton channelName="Informações"/>
    <ChannelButton selected channelName="sala-01"/>
    <ChannelButton channelName="sala-02"/>
    <ChannelButton channelName="sala-03"/>
  </div>
</template>

<script>

  import ChannelButton from './ChannelButton';
  import AddCategoryIcon from 'vue-material-design-icons/Plus'

export default {
  components: {
    ChannelButton,
    AddCategoryIcon
  }
}
</script>

<style scoped lang="scss">
.container{
  grid-area: CL;
  display: flex;
  flex-direction: column;
  padding: 24px 10px 0 16px;
  background: var(--secondary);
}

.category{
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 6px;
  color: var(--grey);
  font-size: 12px;
  font-weight: 500;
  text-transform: uppercase;
  .category-icon{
    color: var(--symbol);
    cursor: pointer;
  }
}

</style>
