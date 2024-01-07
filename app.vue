<template>
  <div>
    <BNavbar toggleable="lg"
             variant="success"
             v-b-color-mode="'dark'">
      <BNavbarBrand href="#">Nuxt Bootstrap Starter</BNavbarBrand>
      <BNavbarToggle target="nav-collapse" />
      <BCollapse id="nav-collapse"
                 is-nav>
        <BNavbarNav>
          <BNavItem href="#">Link</BNavItem>
          <BNavItem href="#"
                    disabled>Disabled</BNavItem>
        </BNavbarNav>
        <!-- Right aligned nav items -->
        <BNavbarNav class="ms-auto mb-2 mb-lg-0">
          <BNavItemDropdown text="Lang"
                            right>
            <BDropdownItem href="#">EN</BDropdownItem>
            <BDropdownItem href="#">ES</BDropdownItem>
            <BDropdownItem href="#">RU</BDropdownItem>
            <BDropdownItem href="#">FA</BDropdownItem>
          </BNavItemDropdown>
          <BNavItemDropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>User</em>
            </template>
            <BDropdownItem href="#">Profile</BDropdownItem>
            <BDropdownItem href="#">Sign Out</BDropdownItem>
          </BNavItemDropdown>
        </BNavbarNav>
        <BNavForm class="d-flex">
          <BFormInput class="me-2"
                      placeholder="Search" />
          <BButton type="submit"
                   variant="outline-success">Search</BButton>
        </BNavForm>
      </BCollapse>
    </BNavbar>
    <NuxtWelcome />
  </div>
</template>
<script setup>
import {vBColorMode} from 'bootstrap-vue-next'
</script>
<style lang="scss">
@use "~/assets/scss/bootstrap.scss";
</style>
