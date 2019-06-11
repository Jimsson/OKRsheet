<template>
  <md-tabs md-alignment="fixed">
    <md-tab id="tab-team" md-label="Team" md-icon="people">
      <members-page></members-page>
    </md-tab>
  </md-tabs>
</template>

<script>
import MembersPage from './teammembers/MembersPage';

export default {
  name: 'team-page',
  components: {MembersPage},
  data: function() {
    return {
      id: ''
    };
  },
  created: function() {
    this.id = this.$router.history.current.params.id;
  },
  methods: {

  }
};
</script>

<style>
.md-tabs.md-alignment-fixed.md-theme-default {
  height: 100%;
}
.md-content.md-tabs-content.md-theme-default {
  height: 100% !important;
}
</style>
