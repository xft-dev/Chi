<template lang="pug">
<TitleBar title="Transfer list" description="Transfer list is used to organize and select items" :tabs="pageTabs" />
.chi-grid__container.-pt--3
  .chi-tabs-panel.-active#examples
    <Examples />
  .chi-tabs-panel#properties
    <Properties />
  .chi-tabs-panel#accessibility
    <Accessibility />
</template>

<script lang="ts">
import { Vue } from 'vue-facing-decorator';
import Examples from './examples/index.vue';

import Properties from './_properties.vue';
import Accessibility from './_accessibility.vue';
import { standardComponentPageTabs } from '@/constants/constants';

@NuxtComponent({
  components: {
    Accessibility,
    Examples,
    Properties,
  },
})
export default class TransferList extends Vue {
  pageTabs = standardComponentPageTabs;
}
</script>
