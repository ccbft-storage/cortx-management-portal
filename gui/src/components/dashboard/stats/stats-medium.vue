/*
* CORTX-CSM: CORTX Management web and CLI interface.
* Copyright (c) 2020 Seagate Technology LLC and/or its Affiliates
* This program is free software: you can redistribute it and/or modify
* it under the terms of the GNU Affero General Public License as published
* by the Free Software Foundation, either version 3 of the License, or
* (at your option) any later version.
* This program is distributed in the hope that it will be useful,
* but WITHOUT ANY WARRANTY; without even the implied warranty of
* MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
* GNU Affero General Public License for more details.
* You should have received a copy of the GNU Affero General Public License
* along with this program. If not, see <https://www.gnu.org/licenses/>.
* For any questions about this software or licensing,
* please email opensource@seagate.com or cortx-questions@seagate.com.
*/
<template>
  <div id="statsContainer">
    <div style="height: 30px;">
      <div class="cortx-text-lg cortx-text-bold cortx-float-l" id="stats-performance">Performance</div>
      <img
        id="stats-medium-zoomicon"
        :src="require('@/assets/zoom-in.svg')"
        @click="$router.push('/performance')"
        class="cortx-float-r cortx-cursor-pointer"
      />
    </div>
    <cortx-line-chart chartId="line_chart" />
  </div>
</template>
<script lang="ts">
import { Component, Vue, Prop, Mixins } from "vue-property-decorator";
import * as c3 from "c3";
import { PerformanceStatsQueryParams } from "./../../../models/performance-stats";
import CortxLineChart from "./../../widgets/line-chart.vue";
@Component({
  name: "cortx-stats-medium",
  components: {
    cortxLineChart: CortxLineChart
  }
})
export default class CortxStatsMedium extends Vue {}
</script>
<style lang="scss" scoped></style>
