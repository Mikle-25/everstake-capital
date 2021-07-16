<template>
  <b-container class="col-6 d-flex flex-column align-items-center">
    <h1 class="align-self-start mt-5 mb-5">Get started with Everstake Capital</h1>

    <b-form @submit="postData" class="row gy-4">
      <b-form-group class="col-6" label="First name" label-for="First name">
        <b-form-input
          id="First name"
          name="First name"
          v-model.trim="form.firstName"
          required
          placeholder="First name"
        >
        </b-form-input>
      </b-form-group>

      <b-form-group class="col-6" label="Last name" label-for="Last name">
        <b-form-input
          id="Last name"
          name="Last name"
          v-model.trim="form.lastName"
          placeholder="Last name"
        ></b-form-input>
      </b-form-group>

      <b-form-group class="col-6" label="Country" label-for="country">
        <b-form-input
          id="country"
          name="Country"
          v-model.trim="form.country"
          required
          placeholder="USA"
        ></b-form-input>
      </b-form-group>

      <b-form-group class="col-6" label="Email address" label-for="Email address">
        <b-form-input
          id="Email address"
          name="Email"
          type="email"
          v-model.trim="form.email"
          required
          placeholder="example@gmail.com"
        ></b-form-input>
      </b-form-group>

      <b-form-group class="col-6" label="Company/Organization" label-for="company">
        <b-form-input
          id="company"
          name="Company/Organization"
          v-model.trim="form.company"
          required
        ></b-form-input>
      </b-form-group>

      <div class="col-12">
        <b-button class="col-3" type="submit" variant="dark" :disabled="loading">Submit</b-button>
      </div>
    </b-form>

    <MediaList />
  </b-container>
</template>

<script>
import MediaList from '../components/MediaList.vue';

export default {
  name: 'Form',
  components: { MediaList },
  data() {
    return {
      loading: false,
      form: {
        firstName: '',
        lastName: '',
        country: '',
        company: '',
        email: '',
      },
    };
  },
  methods: {
    async postData(event) {
      event.preventDefault();

      try {
        this.loading = true;
        await fetch(process.env.VUE_APP_GOOGLE_SHEETS_API, {
          method: 'POST',
          body: new FormData(event.target),
        });
      } catch (e) {
        console.error(e);
      } finally {
        this.form.firstName = '';
        this.form.lastName = '';
        this.form.country = '';
        this.form.company = '';
        this.form.email = '';
        this.loading = false;
      }
    },
  },
};
</script>

<style scoped></style>
