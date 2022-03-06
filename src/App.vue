<template>
  <help-form>
    <template v-slot:help>
      <p>{{ help_text }}</p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="email" />
      <input type="text" placeholder="username" />
      <input type="password" password="password" />
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
    <p>Some text</p>
  </help-form>
  <help-form>
    <template v-slot:help>
      <p>Contact help text</p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="name" />
      <input type="text" placeholder="message" />
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
  </help-form>
</template>

<script>
import HelpForm from "./components/HelpFormComponent.vue";

export default {
  name: "App",
  components: {
    HelpForm,
  },
  data() {
    return {
      help_text: "This is some help text.",
    };
  },
};
</script>
