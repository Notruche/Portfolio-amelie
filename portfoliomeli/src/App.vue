<template>
  <div id="app">
    <div class="row container-fluid">
      <div class="col-2 head p-0">
        <div class="position-relative">
          <img src="../src/assets/img/titres/fond.png" alt="head" />
          <img src="../src/assets/img/titres/ameliepecot.png" alt="img" class="mt-4" />
          <div class="bg-white mt-5 mb-5">
            <img
              :src="illu"
              alt="bd"
              v-on:mouseover="hoverillu()"
              v-on:mouseleave="illuleave()"
              v-on:click="pageillu()"
            />
            <img
              :src="bd"
              alt="bd"
              v-on:mouseover="hoverbd()"
              v-on:mouseleave="bdleave()"
              v-on:click="pagebd()"
            />
            <img
              :src="bazar"
              alt="bd"
              v-on:mouseover="hoverbazar()"
              v-on:mouseleave="bazarleave()"
              v-on:click="pagebazar()"
            />
            <img
              :src="contact"
              alt="bd"
              v-on:mouseover="hovercontact()"
              v-on:mouseleave="contactleave()"
              v-on:click="pagecontact()"
            />
            <img
              :src="apropos"
              alt="bd"
              v-on:mouseover="hoverapropos()"
              v-on:mouseleave="aproposleave()"
              v-on:click="pageapropos()"
            />
          </div>
          <a href="https://www.instagram.com/pekollio/" target="blank">
            <img src="../src/assets/img/titres/instagram.png" alt="bd" />
          </a>
        </div>
      </div>
      <div class="col-3 illusion"></div>
      <div v-if="illustration" class="col-8 row container-fluid">
        <div class="col-6">
          <img src="../src/assets/img/illus/memoire.gif" alt="illu" />
          <img src="../src/assets/img/illus/cartes.png" alt="illu" />
          <img src="../src/assets/img/illus/buche.png" alt="illu" />
          <img src="../src/assets/img/illus/champis.gif" alt="illu" />
          <img src="../src/assets/img/illus/animaux.png" alt="illu" />
          <img src="../src/assets/img/illus/inktober.png" alt="illu" />
          <img src="../src/assets/img/illus/liens.png" alt="illu" />
        </div>
        <div class="col-6">
          <img src="../src/assets/img/illus/attenteA5.png" alt="illu" />
          <img src="../src/assets/img/illus/sérigraphie.jpg" alt="illu" />
          <img src="../src/assets/img/illus/expo.png" alt="illu" />
          <img src="../src/assets/img/illus/rubikpeint.png" alt="illu" />
          <img src="../src/assets/img/illus/peur.png" alt="illu" />
          <img src="../src/assets/img/illus/yokai.png" alt="illu" />
          <img src="../src/assets/img/illus/demons.png" alt="illu" />
          <img src="../src/assets/img/illus/elly.png" alt="illu" />
        </div>
      </div>
      <div v-if="bande" class="col-8 row container-fluid">
        <div class="col-6">
          <img src="../src/assets/img/bd/ellysyno.gif" alt="illu" />
          <img src="../src/assets/img/bd/rubikssyno.gif" alt="illu" />
          <img src="../src/assets/img/bd/gribousyno.gif" alt="illu" />
        </div>
        <div class="col-6">
          <img src="../src/assets/img/bd/babysyno.gif" alt="illu" />
          <img src="../src/assets/img/bd/campingsyno.gif" alt="illu" />
          <img src="../src/assets/img/bd//courtesyno.gif" alt="illu" />
        </div>
      </div>
      <div v-if="baz" class="col-8 row container-fluid">
        <h1>EN CONSTRUCTION</h1>
      </div>
            <div v-if="conta" class="col-8 row container-fluid">
              <h1>EN CONSTRUCTION</h1>
      </div>
            <div v-if="aprop" class="col-8 row container-fluid">
              <h1>EN CONSTRUCTION</h1>
      </div>
      <div class="col-1"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      illu: require("../src/assets/img/titres/illustrationor.png"),
      bd: require("../src/assets/img/titres/bd.png"),
      bazar: require("../src/assets/img/titres/bazar.png"),
      contact: require("../src/assets/img/titres/contact.png"),
      apropos: require("../src/assets/img/titres/apropos.png"),
      illustration: true,
      bande: false,
      baz: false,
      conta: false,
      aprop: false
    };
  },
  methods: {
    hoverillu() {
      var that = this;
      if (that.illustration == false) {
        that.illu = require("../src/assets/img/titres/illustrationhover.png");
      }
    },
    illuleave() {
      var that = this;
      if (that.illustration == false) {
        that.illu = require("../src/assets/img/titres/illustration.png");
      }
    },
    hoverbd() {
      var that = this;
      if (that.bande == false) {
        that.bd = require("../src/assets/img/titres/bdhover.png");
      }
    },
    bdleave() {
      var that = this;
      if (that.bande == false) {
        that.bd = require("../src/assets/img/titres/bd.png");
      }
    },
    hoverbazar() {
      var that = this;
      if (that.baz == false) {
        that.bazar = require("../src/assets/img/titres/bazarhover.png");
      }
    },
    bazarleave() {
      var that = this;
      if (that.baz == false) {
        that.bazar = require("../src/assets/img/titres/bazar.png");
      }
    },
    hovercontact() {
      var that = this;
      if (that.conta == false) {
        that.contact = require("../src/assets/img/titres/contacthover.png");
      }
    },
    contactleave() {
      var that = this;
      if (that.conta == false) {
        that.contact = require("../src/assets/img/titres/contact.png");
      }
    },
    hoverapropos() {
      var that = this;
      if (that.aprop == false) {
        that.apropos = require("../src/assets/img/titres/aproposhover.png");
      }
    },
    aproposleave() {
      var that = this;
      if (that.aprop == false) {
        that.apropos = require("../src/assets/img/titres/apropos.png");
      }
    },
    pageillu() {
      this.illu = require("../src/assets/img/titres/illustrationor.png");
      this.bd = require("../src/assets/img/titres/bd.png");
      this.bazar = require("../src/assets/img/titres/bazar.png");
      this.contact = require("../src/assets/img/titres/contact.png");
      this.apropos = require("../src/assets/img/titres/apropos.png");
      this.illustration = true;
      this.bande = false;
      this.baz = false;
      this.conta = false;
      this.aprop = false;
    },
    pagebd() {
      this.bd = require("../src/assets/img/titres/bdor.png");
      this.illu = require("../src/assets/img/titres/illustration.png");
      this.bazar = require("../src/assets/img/titres/bazar.png");
      this.contact = require("../src/assets/img/titres/contact.png");
      this.apropos = require("../src/assets/img/titres/apropos.png");
      this.illustration = false;
      this.bande = true;
      this.baz = false;
      this.conta = false;
      this.aprop = false;
    },
    pagebazar() {
      this.bazar = require("../src/assets/img/titres/bazaror.png");
      this.bd = require("../src/assets/img/titres/bd.png");
      this.illu = require("../src/assets/img/titres/illustration.png");
      this.contact = require("../src/assets/img/titres/contact.png");
      this.apropos = require("../src/assets/img/titres/apropos.png");
      this.illustration = false;
      this.bande = false;
      this.baz = true;
      this.conta = false;
      this.aprop = false;
    },
    pagecontact() {
      this.contact = require("../src/assets/img/titres/contactor.png");
      this.bd = require("../src/assets/img/titres/bd.png");
      this.bazar = require("../src/assets/img/titres/bazar.png");
      this.illu = require("../src/assets/img/titres/illustration.png");
      this.apropos = require("../src/assets/img/titres/apropos.png");
      this.illustration = false;
      this.bande = false;
      this.baz = false;
      this.conta = true;
      this.aprop = false;
    },
    pageapropos() {
      this.apropos = require("../src/assets/img/titres/a propos or.png");
      this.bd = require("../src/assets/img/titres/bd.png");
      this.bazar = require("../src/assets/img/titres/bazar.png");
      this.contact = require("../src/assets/img/titres/contact.png");
      this.illu = require("../src/assets/img/titres/illustration.png");
      this.illustration = false;
      this.bande = false;
      this.baz = false;
      this.conta = false;
      this.aprop = true;
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
