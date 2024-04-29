<script setup>
import { ref } from "vue";

let num = ref(0);
</script>

<template>
    <nav
        class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom border-body"
    >
        <div class="container-fluid">
            <!-- <a class="navbar-brand" href="#">Pokedéx</a> -->
            <router-link class="navbar-brand" aria-current="page" to="/">
                Rick & Morty API
            </router-link>
            <button
                class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarNav"
                aria-controls="navbarNav"
                aria-expanded="false"
                aria-label="Toggle navigation"
            >
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <router-link
                            class="nav-link"
                            aria-current="page"
                            to="/"
                        >
                            Início
                        </router-link>
                    </li>
                    <li class="nav-item">
                        <router-link
                            class="nav-link"
                            aria-current="page"
                            to="/about"
                        >
                            Sobre
                        </router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <div class="main">
        <router-view></router-view>
    </div>

    <footer class="bg-dark text-light">
      <div>Unimar | ADS | {{ new Date().getFullYear() }}</div>
    </footer>
</template>


<style>
footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
}
</style>  