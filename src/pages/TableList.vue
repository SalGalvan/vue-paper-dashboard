<template>
  <div class="row">
    <div class="col-12">
      <card :title="table1.title" :subTitle="table1.subTitle">
        <div slot="raw-content" class="table-responsive">
          <paper-table :data="table1.data" :columns="table1.columns">
          </paper-table>
        </div>
      </card>
    </div>

    <div class="col-12">
      <card class="card-plain">
        <div class="table-full-width table-responsive">
          <paper-table
            type="hover"
            :title="table2.title"
            :sub-title="table2.subTitle"
            :data="table2.data"
            :columns="table2.columns"
          >
          </paper-table>
        </div>
      </card>
    </div>
  </div>
</template>
<script>
import { PaperTable } from "@/components";
const tableColumns = ["Id", "Name", "Status", "Region", "Title"];
const tableData = [
  {
    id: 1,
    name: "Sal Galvan",
    status: "Full Time",
    region: "North America",
    title: "Technical Analyst",
  },
  {
    id: 2,
    name: "Britney Davis",
    status: "Full Time",
    region: "North America",
    title: "Project Manager",
  },
  {
    id: 3,
    name: "Tim Robinson",
    status: "Full Time",
    region: "North America",
    title: "Quality Analyst",
  },
  {
    id: 4,
    name: "Rim Jimenez",
    status: "Contractor",
    region: "North America",
    title: "Business Analyst",
  },
  {
    id: 5,
    name: "Jose Chacon",
    status: "Full Time",
    region: "North America",
    title: "Technical Analyst",
  },
];

export default {
  components: {
    PaperTable,
  },
  data() {
    return {
      table1: {
        title: "Colleagues in Region",
        
        columns: [...tableColumns],
        data: [...tableData],
      },
      table2: {
       
      },
    };
  },
};
</script>
<style></style>
