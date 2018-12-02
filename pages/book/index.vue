<template>
  <el-form
    ref="form"
    :model="form"
    label-width="120px"
  >
    <h1>Book</h1>
    <el-form-item label="Reservator">
      <el-input v-model="form.name"/>
    </el-form-item>
    <el-form-item label="Date">
      <el-col :span="11">
        <el-date-picker
          v-model="form.date"
          type="date"
          placeholder="Pick a date"
          style="width: 100%;"
        />
      </el-col>
    </el-form-item>
    <el-form-item label="Time">
      <el-col :span="11">
        <el-time-picker
          v-model="form.start"
          type="fixed-time"
          placeholder="Pick a start time"
          style="width: 100%;"/>
      </el-col>
      <el-col
        :span="2"
        class="line"
        style="text-align: center"
      >-</el-col>
      <el-col :span="11">
        <el-time-picker
          v-model="form.end"
          type="fixed-time"
          placeholder="Pick a end time"
          style="width: 100%;"/>
      </el-col>
    </el-form-item>
    <el-form-item label="The purpose">
      <el-input
        v-model="form.desc"
        type="textarea" />
    </el-form-item>
    <el-form-item>
      <el-button
        type="primary"
        @click="onSubmit"
      >
        Request
      </el-button>
      <el-button>Clear</el-button>
    </el-form-item>
  </el-form>
</template>

<script>
export default {
  name: 'Index',
  data() {
    return {
      form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
      }
    }
  },
  methods: {
    onSubmit() {
      console.log('submit!')
    }
  }
}
</script>
