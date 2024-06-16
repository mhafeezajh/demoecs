<!-- Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved. -->
<!-- SPDX-License-Identifier: MIT-0 -->

<template>
  <div id="navbar">
    <b-navbar toggleable="lg" type="dark" style="width: auto;" variant="dark" fixed="top">
        <b-navbar-brand>
            <router-link to="/main">
            </router-link>
            <router-link
                class="ml-2"
                to="/main"
                style="color:white"
                >Amazon ECS
            </router-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-nav-form>
                    <b-form-input size="sm" class="mr-sm-2" placeholder="Search for products"></b-form-input>
                    <b-button size="sm" class="my-2 my-sm-0" type="submit" to='/search'>Search</b-button>
                </b-nav-form>

                <b-navbar-nav>
                    <b-nav-item>
                        <router-link
                            class="ml-2"
                            to="/about"
                            style="color:white"
                            >About
                        </router-link>
                    </b-nav-item>
                </b-navbar-nav>

            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Nav",
  methods: {
    async logOutEvent() {
      this.$router.push("/main");
    },
  }
};
</script>

<style scoped>
    .img{
        position: center;
    }
</style>
