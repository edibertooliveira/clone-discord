<template>
  <div class="channel-message" :class="{'has-mention': hasMention}">
    <div class="avatar" :class="{'is-bot': isBot}"></div>
    <div class="message">
      <div class="user">
        <strong>{{author}}</strong>
        <span class="bot" v-if="isBot">Bot</span>
        <span class="date">{{date}}</span>
      </div>
      <div class="body">
        <slot />
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: {
    author: String,
    date: String,
    hasMention: Boolean,
    isBot: Boolean,
    message: String,
  }

}
</script>

<style lang="scss" scoped>
  .channel-message {
    display: flex;
    align-items: center;
    padding: 8px 16px;
    margin-right: 4px;
    background: transparent;
    margin-top: 13px;

    &.has-mention {
      background: var(--mention-message);
      border-left: solid 2px var(--mention-detail);
    }

    &:hover {
      background: var(--secondary);
    }

  }
  .avatar {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: var(--secondary);
    flex-shrink: 0;

    &.is-bot {
      background: var(--mention-detail);
    }
  }
  .message {
    margin-left: 17px;
    height: 40px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    strong {
      color: var(--white);
      font-size: 16px;
    }


    .date {
      margin-left: 6px;
      color: var(--grey);
      font-size: 13px;
    }

    .bot {
      margin-left: 9px;
      background: var(--discord);
      color: var(--white);
      padding: 4px 5px;
      border-radius: 4px;
      text-transform: uppercase;
      font-size: 11px;
      font-weight: bold;

    }

    .body {
      color: var(--white);
      text-align: left;
      font-size: 16px;

      .mention{
        color: var(--link);
        cursor: pointer;

        &:hover {
          text-decoration: underline;
        }
      }
    }
  }

</style>
