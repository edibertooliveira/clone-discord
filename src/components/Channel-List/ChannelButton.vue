<template>
  <div class="container">
    <div class="channel-info">
      <HashTagIcon :size='20'/>
      <div class="">Chat Livre</div>
    </div>
    <div class="channel-actions">
      <InvicteIcon :size='16'/>
      <SettingIcon :size='16'/>
    </div>
  </div>
</template>

<script>
import HashTagIcon from 'vue-material-design-icons/Pound';
import InvicteIcon from 'vue-material-design-icons/AccountPlus';
import SettingIcon from 'vue-material-design-icons/CupOutline';


export default {
  components: {
    HashTagIcon,
    InvicteIcon,
    SettingIcon
  }

}
</script>

<style>


</style>
