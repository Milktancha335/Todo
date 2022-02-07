<template>

  <div class="container">
    <v-contaoner>
      <h1>การบ้าน/งานที่ได้รับมอบหมาย</h1>
      <v-select
        v-model="select"
        :items="items"
        label="--เลือกหัวข้อ--"
        solo
      ></v-select>
      <v-text-field v-model="name" label="รายการ" outlined></v-text-field>
      <v-btn color="success" class="mr-4" @click="validate()">เพิ่ม</v-btn>
      <v-contaoner class="">
        <h1>รายวิชาที่เพิ่ม</h1>
       
      </v-contaoner>
    </v-contaoner>
  </div>
</template>


<script>
export default {
  subject: "",
  work: "",
  data() {
    return {
      select:null,
      name:"",
      items: ["วิชา Web", " วิชา SA", " วิชา ML", "อื่นๆ"],
      selectedItem: 1,
      additems: [
        { text: "วิชา Web Assignment500" },
        { text: "วิชา ML Assignment1" },
        { text: "วิชา ML ออกแบบ" },
        { text: "วิชา Web Assignment501" },
      ],
    };
  },
  props: ["A1"],
  methods: {
    validate() {
      this.$emit("Input", this.select, this.name);
       (this.select = ""), (this.name = "");
    },
  },
};
</script>

<style>
</style>
//รับข้อมูล