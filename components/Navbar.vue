<template>
  <div>
    <b-navbar
      class="is-dark light has-shadow"
      style="
        padding-left: 8vw;
        padding-right: 8vw;
        height: 25px;
        background: #2d3161;
      "
      centered
    >
      <template #start> </template>
      <template #end> </template>

      <template #brand>
        <b-navbar-item
          style="font-weight: 600; font-size: 0.8em"
          :to="{ path: '/' }"
          >Home</b-navbar-item
        >
        <b-navbar-item
          style="font-weight: 600; font-size: 0.8em"
          tag="router-link"
          :to="{ path: '/Homes' }"
        >
          Find a home
        </b-navbar-item>
        <b-navbar-item
          style="font-weight: 600; font-size: 0.8em"
          tag="router-link"
          :to="{ path: '/Partner' }"
        >
          Partner with us
        </b-navbar-item>
        <b-navbar-item
          style="font-weight: 600; font-size: 0.8em"
          tag="router-link"
          :to="{ path: '/About' }"
        >
          About us
        </b-navbar-item>
        <b-navbar-item
          style="font-weight: 600; font-size: 0.8em"
          tag="router-link"
          :to="{ path: '/Help' }"
        >
          Help
        </b-navbar-item>
        <!-- <b-navbar-dropdown label="Info">
        <b-navbar-item href="#"> About </b-navbar-item>
        <b-navbar-item href="#"> Contact </b-navbar-item>
      </b-navbar-dropdown> -->
      </template>
    </b-navbar>

    <div
      class="columns is-white light has-shadow"
      style="
        padding-left: 8vw;
        padding-right: 8vw;
        background: #fff;
        margin: 0;
        border-bottom: 1px solid #e3e3e3;
      "
    >
      <div class="column is-2">
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img
            src="~/assets/logotest2.png"
            style="height: 100%"
            alt="Lightweight UI components for Vue.js based on Bulma"
          />
        </b-navbar-item>
      </div>
      <div class="column">
        <b-field>
          <b-input
            type="number"
            placeholder="Search name, developer or project"
            class="is-expanded"
          ></b-input>
          <p class="control">
            <b-button
              class="is-primary"
              style="background: #feaf11; padding: 2px solid white"
            >
              <b-icon pack="fas" icon="search" size="is-small" />
            </b-button>
          </p>
        </b-field>
      </div>
      <div class="column is-2">
        <div class="buttons">
          <a
            class="button is-rounded is-x"
            tag="router-link"
            :to="{ path: '/Register' }"
          >
            <strong>Sign up</strong>
          </a>
          <a
            class="button is-rounded is-primary"
            tag="router-link"
            :to="{ path: '/Login' }"
          >
            <strong>Sign in</strong>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
