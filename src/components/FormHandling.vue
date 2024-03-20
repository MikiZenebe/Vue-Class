<template>
  <div>
    {{ JSON.stringify(formValues, null, 2) }}
  </div>
  <form
    @submit="submitForm"
    style="display: flex; flex-direction: column; gap: 15px"
  >
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea type="text" id="profile" v-model="formValues.profileSummary" />
    </div>

    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a Country</option>
        <option value="ethiopia">Ethiopia</option>
        <option value="india">India</option>
        <option value="rome">Rome</option>
      </select>
    </div>

    <div>
      <label for="jobLocation">Job Location</label>
      <select id="jobLocation" multiple v-model="formValues.jobLocation">
        <option value="">Select a Country</option>
        <option value="ethiopia">Ethiopia</option>
        <option value="india">India</option>
        <option value="rome">Rome</option>
      </select>
    </div>

    <div>
      <input
        type="checkbox"
        id="remoteWork"
        v-model="formValues.remoteWork"
        true-value="yes"
        false-value="no"
      />
      <label for="remoteWork">Open to remote work?</label>
    </div>

    <div>
      <label>Skill set</label>
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValues.skillset"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValues.skillset"
      />
      <label for="css">CSS</label>
      <input
        type="checkbox"
        id="javascript"
        value="javascript"
        v-model="formValues.skillset"
      />
      <label for="javascript">JS</label>
    </div>

    <div>
      <label>Years of Experience</label>
      <input
        type="radio"
        id="0-2"
        value="0-2"
        v-model="formValues.yearsOfExp"
      />
      <label for="0-2">0-2</label>
      <input
        type="radio"
        id="3-5"
        value="3-5"
        v-model="formValues.yearsOfExp"
      />
      <label for="3-5">3-5</label>
      <input
        type="radio"
        id="6-10"
        value="6-10"
        v-model="formValues.yearsOfExp"
      />
      <label for="6-10">6-10</label>
    </div>

    <div>
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  name: "FormHandling",
  data() {
    return {
      formValues: {
        name: "",
        profile: "",
        country: "",
        jobLocation: [],
        remoteWork: "no",
        skillset: [],
        yearsOfExp: "",
      },
    };
  },

  methods: {
    submitForm(e) {
      e.preventDefault();
      console.log("Form Value", this.formValues);
    },
  },
};
</script>
