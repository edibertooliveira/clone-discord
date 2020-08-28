<template>
  <div class="channel-data">
    <div class="message">
      <ChannelMessage
      author="Ediberto Oliveira"
      date="21/0/2012" isBot hasMention>
      Olá Pessoal! Esta é uma mensagem
      </ChannelMessage>

    </div>

    <div class="input-wrapper">
      <input type="text" placeholder="Conversar em #sala-01">
      <div class="icon">
        <At :size="24" />
      </div>
    </div>
  </div>
</template>

<script>
import ChannelMessage from './Channel-Menssage';
import At from 'vue-material-design-icons/At';

export default {
  components: {
    At,
    ChannelMessage,
  }

}
</script>

<style lang="scss" scoped>
.channel-data {
  grid-area: CD;
  display: flex;
  flex-direction: column;
  flex: 1;
  justify-content: space-between;
  background: var(--primary);
}

.message {
  display: flex;
  flex-direction: column;
  height: calc(100vh - 46px - 68px);
  max-height: calc(100vh - 46px - 68px);
  overflow-y: scroll;

  .channel-message:first-child {
    margin-top: 0;
  }



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

.input-wrapper {
  width: 100%;
  height: 68px;
  padding: 0 16px;

  input {
    width: 100%;
    height: 44px;
    padding: 0 10px 0 57px;
    border-radius: 5px;
    background: var(--white);
    background: var(--chat-input);
    position: relative;

    &::placeholder {
      color: var(--grey);
    }
  }

}
.icon {
    color: var(--grey);
    position: relative;
    top: -50%;
    left: 14px;
    transition: 0.2s;
    width: 24px;
  }

</style>
