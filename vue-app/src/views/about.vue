<template>
  <div class="content-container">
    <div class="content-title-group not-found">
      <h2 class="title">Product Wish List</h2>
      <p>
        This project was created to help represent a fundamental app written
        with Vue. The shopping theme is used throughout the app.
      </p>
      <br />
      <h2 class="title">Resources</h2>
      <ul>
        <li>
          <a href="https://github.com/MicrosoftDocs/mslearn-staticwebapp">
            Code in GitHub
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  async mounted() {
    async function getUserInfo() {
      const response = await fetch('/.auth/me');
      const payload = await response.json();
      const { clientPrincipal } = payload;
      return clientPrincipal;
    }

    console.log(getUserInfo());
  },
};
</script>
