<template lang="pug">
  b-modal#raised-mount(:title="$t('modalAchievement')", size='md', :hide-footer="true")
    .modal-body
      .col-12
        // @TODO: +achievementAvatar('raise',0)
        achievement-avatar.avatar
      .col-6.offset-3.text-center
        p {{ $t('hatchedMountText') }}
        br
        button.btn.btn-primary(@click='close()') {{ $t('huzzah') }}
    achievement-footer
</template>

<style scoped>
  .avatar {
    width: 140px;
    margin: 0 auto;
    margin-bottom: 1.5em;
    margin-top: 1.5em;
  }
</style>

<script>
import bModal from 'bootstrap-vue/lib/components/modal';
import achievementFooter from './achievementFooter';
import achievementAvatar from './achievementAvatar';

export default {
  components: {
    bModal,
    achievementFooter,
    achievementAvatar,
  },
  methods: {
    close () {
      this.$root.$emit('hide::modal', 'raised-mount');
    },
  },
};
</script>
