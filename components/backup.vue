
    <b-navbar
      class="py-2 is-white light has-shadow"
      style="padding-left: 8vw; padding-right: 8vw"
      centered
    >
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img
            src="~/assets/logotest2.png"
            style="height: 100%"
            alt="Lightweight UI components for Vue.js based on Bulma"
          />
        </b-navbar-item>
      </template>
      <template #start>
        <b-input expanded></b-input>
      </template>

      <template #end>
        <b-navbar-item
          style="font-weight: 600"
          tag="router-link"
          :to="{ path: '/' }"
          >Home</b-navbar-item
        >
        <b-navbar-item
          style="font-weight: 600"
          tag="router-link"
          :to="{ path: '/Homes' }"
        >
          Find a home
        </b-navbar-item>
        <b-navbar-item
          style="font-weight: 600"
          tag="router-link"
          :to="{ path: '/Partner' }"
        >
          Partner with us
        </b-navbar-item>
        <b-navbar-item
          style="font-weight: 600"
          tag="router-link"
          :to="{ path: '/About' }"
        >
          About us
        </b-navbar-item>
        <b-navbar-item
          style="font-weight: 600"
          tag="router-link"
          :to="{ path: '/Help' }"
        >
          Help
        </b-navbar-item>
        <!-- <b-navbar-dropdown label="Info">
        <b-navbar-item href="#"> About </b-navbar-item>
        <b-navbar-item href="#"> Contact </b-navbar-item>
      </b-navbar-dropdown> -->
        <b-navbar-item tag="div">
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
        </b-navbar-item>
      </template>
    </b-navbar>
    