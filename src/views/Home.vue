<template>
  <navbar>
    <template v-slot:logo>
      Coffee
    </template>
    <template v-slot:primary-menu>
      <li><a class="brown-text modal-trigger" href="#login-modal">Login</a></li>
      <li><a class="brown-text" href="#">Register</a></li>
    </template>
    <template v-slot:sidenav-trigger>
      <i class="material-icons brown-text">menu</i>
    </template>
    <template v-slot:secondary-menu>
      <li><a class="brown-text" href="#">Drink</a></li>
      <li><a class="brown-text" href="#">Food</a></li>
    </template>
    <template v-slot:sidenav>
      <li><a class="brown-text" href="#">Drink</a></li>
      <li><a class="brown-text" href="#">Food</a></li>
      <li><a class="brown-text" href="#">Login</a></li>
      <li><a class="brown-text" href="#">Register</a></li>
    </template>
  </navbar>

  <div id="login-modal" class="modal">
    <form>
      <div class="modal-content">
        <h4 class="brown-text">Login</h4>
        <div class="row">
          <div class="col s12">
            <div class="row">
              <div class="input-field col s12">
                <i class="material-icons prefix">email</i>
                <input id="email" type="text" class="validate">
                <label for="email">Email</label>
              </div>
              <div class="input-field col s12">
                <i class="material-icons prefix">lock</i>
                <input id="password" type="text" class="validate">
                <label for="password">Password</label>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="modal-footer">
        <a href="#" class="modal-close waves-effect waves btn-flat" style="margin-right: 4px">Close</a>
        <button type="submit" class="brown waves-effect waves-light btn">Login</button>
      </div>
    </form>
  </div>
</template>
<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue"

import { onMounted } from "vue";

export default {
  components: {
    Navbar
  },
  setup() {
    onMounted(() => {
      var modal = document.querySelectorAll('.modal');
      M.Modal.init(modal, {});
    })
  }
}
</script>
