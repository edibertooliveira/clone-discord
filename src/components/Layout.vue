<template>
  <div id="grid">
    <ServerList />
    <ServerName />
    <ChannelList />
    <UserInfo />
    <ChannelInfo />
    <ChannelData />
    <UserList />
  </div>
</template>

<script>

import ServerList from './Server-List';
import ServerName from './Server-Name';
import ChannelList from './Channel-List';
import UserInfo from './User-Info';
import ChannelInfo from './Channel-Info';
import ChannelData from './Channal-Data';
import UserList from './User-List';

export default {
  components: {
    ServerList,
    ServerName,
    ChannelList,
    UserInfo,
    ChannelInfo,
    ChannelData,
    UserList,
  }
};

</script>

<style scoped>
  #grid{
    display: grid;
    height: 100vh;
    grid-template-columns: 71px 240px auto 240px;
    grid-template-rows: 46px auto 52px;
    grid-template-areas:
    'SL SN CI CI'
    'SL CL CD UL'
    'SL UI CD UL';

  }
</style>
