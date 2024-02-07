<template>
  <div>
    <div>
      <pre>
        {{ JSON.stringify(formValues, null, 2) }}
      </pre>
    </div>
    <form @submit.prevent="submitForm">
      <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model.trim.lazy="formValues.name" />
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

      <div>
        <input
          type="checkbox"
          name=""
          id="remoteWork"
          v-model="formValues.remoteWork"
          true-value="yes"
          false-value="no"
        />
        <label for="remoteWork">Remote Work?</label>
      </div>

      <div>
        <label for="">Skill Set</label>
        <input
          type="checkbox"
          v-model="formValues.skillSet"
          name=""
          id="html"
          value="html"
        />
        <label for="html">HTML</label>
        <input
          type="checkbox"
          v-model="formValues.skillSet"
          name=""
          id="css"
          value="css"
        />
        <label for="css">css</label>
        <input
          type="checkbox"
          v-model="formValues.skillSet"
          name=""
          id="javascript"
          value="javascript"
        />
        <label for="javascript">javascript</label>
      </div>

      <div>
        <label for="">Years of Experience</label>
        <input
          type="radio"
          v-model="formValues.yearsOfExperience"
          name=""
          id="0-2"
          value="0-2"
        />
        <label for="0-2">0-2</label>
        <input
          type="radio"
          v-model="formValues.yearsOfExperience"
          name=""
          id="3-5"
          value="3-5"
        />
        <label for="3-5">3-5</label>
        <input
          type="radio"
          v-model="formValues.yearsOfExperience"
          name=""
          id="6-10"
          value="6-10"
        />
        <label for="6-10">6-10</label>
      </div>

      <div>
        <label for="age">Age</label>
        <input
          type="number"
          name=""
          id="age"
          @keyup.enter="submitForm"
          v-model.number="formValues.age"
        />
      </div>

      <!-- <button type="submit">Submit</button> -->
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
        remoteWork: "no",
        skillSet: [],
        yearsOfExperience: "",
        age: null,
      },
    };
  },
  methods: {
    submitForm() {
      console.log(this.formValues);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
