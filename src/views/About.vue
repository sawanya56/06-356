<template  >
  <div class="bb">
    <div>
      <table class="table">
        <thead>
          <tr>
            <th scope="col">ชื่ออาหาร</th>
            <th scope="col">ราคา</th>
            <th scope="col">จำนวน</th>
            <th scope="col">รวม</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(mi, index) in data" :key="index">
            <td>{{ mi.name }}</td>
            <td>{{ mi.price }}</td>
            <td>{{ mi.value }}</td>
            <td>{{ mi.Total }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-11"></div>
        <div class="col align-self-end">{{ Total }}บาท</div>
      </div>
    </div>

    <b-card bg-variant="light">
      <b-form-group
        label-cols-lg="2"
        label="ข้อมูลลูกค้า"
        label-size="lg"
        label-class="font-weight-bold pt-0"
        class="mb-0"
      >
        <b-form-group
          label="ชื่อ-นามสกุล"
          label-for="nested-street"
          label-cols-sm="3"
          label-align-sm="right"
        >
          <b-form-input id="nested-street"></b-form-input>
        </b-form-group>

        <b-form-group
          label="ที่อยู่"
          label-for="nested-city"
          label-cols-sm="3"
          label-align-sm="right"
        >
          <b-form-input id="nested-city"></b-form-input>
        </b-form-group>

        <b-form-group
          label="เบอร์โทรศัพท์"
          label-for="nested-state"
          label-cols-sm="3"
          label-align-sm="right"
        >
          <b-form-input id="nested-state"></b-form-input>
        </b-form-group>
      </b-form-group>
    </b-card>
  </div>
</template>

<style>
.bb {
  color: rgb(0, 0, 0);
  background-color: rgb(95, 94, 94);
}
</style>
<script>
export default {
  props: {
    data: Array,
    Total: Number,
  },
};
</script>