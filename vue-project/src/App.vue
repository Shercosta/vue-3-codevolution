<template>
  <div>
    <div>
      <pre>
        {{ JSON.stringify(formValues, null, 2) }}
      </pre>
    </div>
    <form>
      <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model="formValues.name" />
      </div>

      <div>
        <label for="profile">Profile Summary</label>
        <textarea
          name=""
          id="profile"
          v-model="formValues.profileSummary"
          cols="30"
          rows="10"
        ></textarea>
      </div>

      <div>
        <label for="country">Country</label>
        <select name="" id="country" v-model="formValues.country">
          <option value="">Select a country</option>
          <option value="india">india</option>
          <option value="vietnam">vietnam</option>
          <option value="singapore">singapore</option>
        </select>
      </div>

      <div>
        <label for="job-location">Job Location</label>
        <select
          name=""
          id="job-location"
          multiple
          v-model="formValues.jobLocation"
        >
          <option value="india">india</option>
          <option value="vietnam">vietnam</option>
          <option value="singapore">singapore</option>
        </select>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
      },
    };
  },
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
