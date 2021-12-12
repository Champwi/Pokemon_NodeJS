<template>

<!-- Les exercices réalisés durant le cours ont été mis en commentaires. Le code actif est le rendu final sur Pokemon -->

  <div class="fond">
    <link
      rel="stylesheet"
      href="http://code.ionicframework.com/ionicons/2.0.1/css/ionicons.min.css"
    />
    <link
      href="https://fonts.googleapis.com/css?family=Roboto:300,400,700"
      rel="stylesheet"
    />
    <div class="card systeme_onglets">
      <div class="intro">
        <div class="titre">
          <h1>évangelyne Rosenbach</h1>
          <span>“Ma seule liberté est de rêver, alors je rêve de liberté.”</span>
        </div>
        <img class="groupe" src="https://zupimages.net/up/17/31/26ub.png" alt="pleiade" />
        <div class="clear"></div>
        <div class="triangle"></div>
      </div>

      <div class="eva">
        <div class="infoeva">
          <img class="icoeva" src="https://image.ibb.co/fKRriQ/94.jpg" alt="eva" />
          <div class="nv">NV</div>
          <div class="nvc">06</div>
          <div class="zoom">
            <a
              href="http://dusk-lumiris.forumactif.com/t4-groupes-progression"
              target="blank"
              ><i class="icon icon ion-search"></i
            ></a>
          </div>
        </div>
        <div class="critere">
          <div class="col2">
            <span>18 ans <i class="icon icon ion-person"></i></span>
            <span>Née le 14 décembre <i class="icon ion-android-list"></i></span>
            <span>étudiante <i class="icon ion-briefcase"></i></span>
            <span>Célibataire <i class="icon ion-heart"></i></span>
          </div>
          <div class="col2">
            <span>Féminin <i class="icon ion-female"></i></span>
            <span>Originaire de lumiris <i class="icon ion-ios-world"></i></span>
            <span>Illumis <i class="icon ion-flag"></i></span>
            <span>Hétérosexuel <i class="icon ion-arrow-swap"></i></span>
          </div>
          <div class="clear"></div>
        </div>
        <div class="clear"></div>
      </div>
      <div class="inventaire">
        <div class="headinv">
          <div class="titre">
            <h2>Pokedex</h2>
          </div>
          <div class="onglets">
            <span
              class="onglet_0 onglet"
              id="onglet_conso"
              onclick="javascript:change_onglet('conso');"
              ><i class="icon ion-ios-briefcase"></i
            ></span>
            <span
              class="onglet_0 onglet"
              id="onglet_rare"
              onclick="javascript:change_onglet('rare');"
              ><i class="icon ion-android-star"></i
            ></span>
            <span
              class="onglet_0 onglet"
              id="onglet_acc"
              onclick="javascript:change_onglet('acc');"
              ><i class="icon ion-bowtie"></i
            ></span>
            <span
              class="onglet_0 onglet"
              id="onglet_capa"
              onclick="javascript:change_onglet('capa');"
              ><i class="icon ion-ios-book"></i
            ></span>
          </div>
          <div class="clear"></div>
          <div class="triangle"></div>
        </div>
        <div class="contenu contenu_onglets">
          <h1>Pokemon</h1>

          <p>Numéro du pokémon ( a insérer ici ):</p>
          <input type="text" v-on:change="pokemonsearch" />
          <b><p>pokemon id</p></b>
          <p>{{ this.idpk }}</p>
          <b><p>Nom pokemon</p></b>
          <p>{{ this.namepk }}</p>

          <ul>
            <li v-for="value in this.typepk">
              <b><p>Pokemon Type</p></b>
              {{ value.type.name }}
            </li>
          </ul>

          <li>
            <ul>
              <b><p>Version classique:</p></b>
            </ul>
            <ul>
              <img id="picdef" />
            </ul>
          </li>
          <li>
            <ul>
              <b> <p>Version Shiny:</p></b>
            </ul>
            <ul>
              <img id="picshin" />
            </ul>
          </li>
        </div>
      </div>

      <div class="collection">
        <div class="badges">
          <img src="https://www.zupimages.net/up/18/41/e8u1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
        </div>
        <div class="rubans">
          <img src="https://www.zupimages.net/up/18/52/qfah.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
          <img src="https://www.zupimages.net/up/18/04/00t1.png" alt="badge" />
        </div>
        <div class="clear"></div>
      </div>

      <div class="inventaire">
        <div class="headinv">
          <div class="titre">
            <h2>Inventaire</h2>
          </div>
        </div>

        <div class="onglets" style="border: solid 1px #e0e0e0; margin-top: -1px">
          <div class="sacados" style="margin-top: 30px">
            <div class="objets">
              <h1>Objets</h1>
              <div class="listobjets" style="width: 95%">
                <img src="https://www.zupimages.net/up/17/11/ldfl.png" alt="poke" /> x16
                Pokeballs<br />
                <img
                  src="http://www.pokepedia.fr/images/0/0c/Plaquesprit.png"
                  alt="journal"
                />
                x8 poké. sucré<br />
                <img src="https://www.zupimages.net/up/17/13/kna8.png" /> x12 Laits<br />
                <img src="http://www.pokepedia.fr/images/2/2d/Miel.png" /> x1 Super
                Miel<br />
                <img src="https://www.pokepedia.fr/images/8/8e/Super_Bonbon.png" /> x4
                Superbonbon<br />
                <img src="http://www.pokepedia.fr/images/8/87/Ticketmystik.png" /> x4
                entrainement intensif<br />
                <img src="https://www.pokepedia.fr/images/9/91/Miniat_Ticket_Duo.png" />
                x1 coupon de reduction<br />
                <img src="http://www.pokepedia.fr/images/e/e7/Bicyclette.png" /> x1
                Bicyclette<br />
                <img src="http://www.pokepedia.fr/images/c/c0/Cryoz%C3%A9lite.png" /> x1
                Cryozélite<br />
                <img src="https://www.pokepedia.fr/images/3/33/Aquaz%C3%A9lite.png" /> x1
                Aquazélite<br />
                <img
                  src="https://www.pokepedia.fr/images/2/22/Miniat_Voltaz%C3%A9lite.png"
                />
                x1 Voltazélite<br />
                <img src="http://www.pokepedia.fr/images/5/52/Miniat_Roucarnagite.png" />
                x1 Roucarnagite<br />
                <img src="http://www.pokepedia.fr/images/2/29/Miniat_Pharampite.png" /> x1
                Pharampite<br />
                <img src="https://www.pokepedia.fr/images/b/ba/Miniat_Laggronite.png" />
                x1 Laggronite<br />
                <img src="http://www.pokepedia.fr/images/5/52/Parure_Rubans.png" /> x1
                Rubans <br />
                <img src="http://www.pokepedia.fr/images/4/48/Parure_Bouton_Rond.png" />
                x1 Perle <br />
                <img src="http://www.pokepedia.fr/images/f/fb/Parure_Petit_Chapeau.png" />
                x1 Chapeau <br />
                <img src="http://www.pokepedia.fr/images/4/45/Parure_Cape_Blanche.png" />
                x1 Cape <br />
              </div>
            </div>
            <div class="capacite">
              <h1>Capacités</h1>
              <div class="listcap">
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT17 Abri (U) <br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT83 Harcèlement <br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_poison.png"
                  alt="cs"
                />
                CT84 Direct-Toxic (U)<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT87 Vantardise<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_psy.png"
                  alt="cs"
                />
                CT88 Blabla Dodo (U)<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT90 Clonage<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT91 Luminocanon<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_electrik.png"
                  alt="ct"
                />
                CT93 Eclair Fou (U)<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT94 Force Cachée (U)<br />
                <img
                  src="https://www.pokebip.com/pages/icones/objets/ct_normal.png"
                  alt="ct"
                />
                CT95 Aboiement<br />
              </div>
            </div>
            <div class="talents">
              <h1>talents</h1>
              <div class="listalent" style="height: 145px">
                Nv 2 : Contribution au Bonheur. <br />
                Nv 3 : Chance <br />Nv 4 : Capsule secrète<br />
                Nv 5 : Capture gratuite <br />Nv 6 : Pension et Reproduction<br />
                Nv 7 : Super boutique <br />Nv 8 : Capacités par Reproduction
              </div>
            </div>
            <div class="clear"></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!--Exo 1 
  
  <div>
   <h1> pokemon</h1>
   <div v-if="isActive" id="hide">
   </div>
   <img src ="../assets/aesop.jpg" id="img1"/>
   <button v-on:click="img">Changer l'image</button>
  </div>-->

  <!--Exo 2
<div>
  <button v-on:click="isActive = !isActive">button</button>
<div v-if="isActive" id="hide">
<p>Cacher moi</p>
</div>
</div> -->

  <!--Exo 3 <div>
<img src ="../assets/aesop.jpg" id="img1"/>
<button v-on:click="img">Changement img</button>
<button v-on:click="text">Bouton ajout</button>
</div>-->

  <!--Exo 4-->

  <!--
<div>
<input id="pokemonbox" type="text" v-on:change='pokemonsearch'>
<p>{{this.nom}}</p>
<p>{{this.poids}}</p>
<button v-on:click="text">Bouton ajout</button>
</div>

</template>

<script>
import axios from 'axios';

export default {
  name: 'HelloWorld',
  data () {
    return {
      show : true,
      isActive : true,
      info: null,
      nom:null,
      taille:null,
    }
  },
  
  methods :{
toggle : function(){
  console.log("isActive");
  this.isActive =!this.Active;
},

img : function(){
  var i = document.getElementById("img1");
  var j = i.getAttribute("src");
  console.log(j)
  if (j =="/static/kazuha.png") {
    j = "../assets/aesop.jpg";
  } else {
    j ="/static/sabito.jpg";
}
i.setAttribute("src", j);
},

text:function(){
  var btn = document.createElement("BUTTON");
  btn.innerHTML = "CLICK ME";
  document.body.appendChild(btn);
},

pokemonsearch: function(){
  var i = document.getElementById('pokedex').value

  axios
  .get('https://pokeapi.co/api/v2/pokemon' + i)
  .then(response => {
    this.info = response
    this.nom = response.name
    this.poids = response.size
  })
},

mounted(){
  axios
  .get('https://pokeapi.co/api/v2/pokemon/1')
  .then(response =>(this.info = response))
}
  }
}

</script>-->
</template>

<script>
import axios from "axios";
export default {
  name: "HelloWorld",
  data() {
    return {
      show: true,
      change: true,
      message: "",
      items: [],
      nextNum: 1,
      info: null,
      idpk: null,
      typepk: null,
      namepk: null,
      imgpk: null,
    };
  },
  methods: {
    pokemonsearch: function (event) {
      var url = "https://pokeapi.co/api/v2/pokemon/" + event.target.value;
      console.log(url);
      axios.get(url).then((reponse) => {
        this.idpk = reponse.data.id;
        this.typepk = reponse.data.types;
        this.namepk = reponse.data.name;
        this.defaultimgpk = reponse.data.sprites.front_default;
        document.getElementById("picdef").src = this.defaultimgpk;
        this.shinyimgpk = reponse.data.sprites.front_shiny;
        document.getElementById("picshin").src = this.shinyimgpk;
      });
    },
  },
  mounted() {
    axios
      .get("http://pokeapi.co/api/v2/pokemon/1")
      .then((reponse) => (this.info = reponse));
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
table {
  text-align: center;
}

body {
  background: #f2f2f2;
  color: #636363;
}

.card {
  margin: 0 auto;
  width: 680px;
}

.clear {
  clear: both;
}

.intro {
  background: url("https://zupimages.net/up/18/33/xyz0.png") 80% 80% #f8f8f8 no-repeat;
  border: 1px solid #e6e6e6;
  padding: 30px 20px;
  position: relative;
  overflow: hidden;
}
.intro .titre {
  width: 80%;
  float: left;
}

.intro .titre h1 {
  font-family: roboto;
  font-style: italic;
  color: #b474c2;
  text-transform: lowercase;
  border-bottom: 1px solid #e6e6e6;
  margin: 0;
}

.intro .titre span {
  text-align: right;
  display: block;
  text-transform: uppercase;
  font-family: roboto;
  font-size: 9px;
  color: #636363;
  margin-top: 5px;
}

.intro .groupe {
  margin-left: 10%;
  margin-right: 1%;
  float: right;
  position: relative;
  z-index: 10;
}

.intro .triangle {
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 0 0 1000px 400px;
  border-color: transparent transparent #b474c2 transparent;
  position: absolute;
  top: -200px;
  right: 0;
  z-index: 1;
}

.eva {
  background: white;
  border: 1px solid #e6e6e6;
  padding: 20px;
  margin-top: 10px;
}

.eva .infoeva {
  position: relative;
  width: 23%;
  float: left;
  text-align: right;
}

.eva .infoeva .icoeva {
  border-radius: 100px;
  background: #f8f8f8;
  padding: 5px;
  border: 1px solid #e6e6e6;
  position: relative;
  z-index: 2;
  margin-left: 13%;
}

.eva .infoeva .nv {
  text-transform: uppercase;
  font-size: 14px;
  font-family: roboto;
  background: #f8f8f8;
  border-radius: 100px;
  padding: 10px;
  width: 20px;
  z-index: 1;
  position: absolute;
  top: 30px;
  left: 0;
}

.eva .infoeva .nvc {
  text-transform: uppercase;
  font-size: 16px;
  font-family: roboto;
  background: #b474c2;
  border-radius: 100px;
  padding: 10px;
  width: 20px;
  color: white;
  z-index: 3;
  position: absolute;
  top: 55px;
  left: 18px;
}

.eva .infoeva .zoom {
  text-transform: uppercase;
  font-size: 14px;
  font-family: roboto;
  background: #e9e9e9;
  border-radius: 100px;
  padding: 8px;
  width: 12px;
  z-index: 4;
  position: absolute;
  top: 82px;
  left: 42px;
  height: 14px;
  padding-top: 6px;
}

.eva .critere {
  width: 75%;
  float: right;
  height: 110px;
}

.eva .critere .col2 {
  width: 45%;
  float: left;
  margin-left: 5%;
}

.eva .critere .col2 span {
  display: block;
  border-bottom: 1px solid #e6e6e6;
  text-transform: uppercase;
  font-size: 9px;
  font-family: roboto;
  text-align: right;
  padding: 5.5px;
}

.eva .critere .col2 span i {
  color: #b474c2;
  font-size: 12px;
  margin-left: 5%;
}

.inventaire .headinv {
  background: url("https://zupimages.net/up/18/33/xyz0.png") 80% 80% #f8f8f8 no-repeat;
  border: 1px solid #e6e6e6;
  border-top: 0px;
  padding: 10px 20px;
  position: relative;
  overflow: hidden;
}

.inventaire .headinv .triangle {
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 0 0 2000px 800px;
  border-color: transparent transparent #b474c2 transparent;
  position: absolute;
  top: -450px;
  right: 0px;
  z-index: 1;
}

.inventaire .headinv .titre {
  width: 60%;
  float: left;
}

.inventaire .headinv .titre h2 {
  font-family: roboto;
  font-style: italic;
  color: #b474c2;
  text-transform: lowercase;
  margin: 0;
  position: relative;
  z-index: 2;
}

.inventaire .headinv .onglets {
  width: 22%;
  float: right;
  z-index: 2;
  position: relative;
}

.inventaire .headinv .onglet_0 {
  background: #eee !important;
  color: #636363 !important;
}

.inventaire .headinv .onglet_1 {
  background: #ddd;
}

.inventaire .headinv .onglets span {
  background: white;
  border-radius: 100px;
  margin: 0 2px;
  padding: 4px;
  color: #b474c2;
  width: 18px;
  text-align: center;
  display: inline-block;
}

.inventaire .contenu {
  border: 1px solid #e6e6e6;
  border-top: 0px;
  background: white;
  padding: 5px;
}

.inventaire .contenu span {
  background: #f8f8f8;
  margin: 4px;
  text-transform: uppercase;
  font-family: roboto;
  font-size: 10px;
  width: 30%;
  display: inline-block;
  margin: 5px 4px;
  padding: 0 5px;
  padding-bottom: 8px;
}

.contenu_onglet {
  display: none;
  height: 125px;
  overflow: auto;
}

.inventaire .contenu span img {
  height: 20px;
  position: relative;
  margin-right: 5px;
  bottom: -5px;
}

.collection {
  background: white;
  border: 1px solid #e6e6e6;
  padding: 20px;
  margin-top: 10px;
}

.collection .badges {
  background: #f8f8f8;
  border: 1px solid #e6e6e6;
  margin-right: 5px;
  padding: 4px;
  width: 55%;
  float: left;
  text-align: center;
}

.collection .rubans {
  background: #f8f8f8;
  border: 1px solid #e6e6e6;
  padding: 4px;
  width: 40%;
  float: right;
  text-align: center;
}

.collection .badges img,
.collection .rubans img {
  width: 31px;
  margin: 0 4px;
}

.equipe .titre {
  background: url("https://zupimages.net/up/18/33/xyz0.png") 80% 80% #f8f8f8 no-repeat;
  border: 1px solid #e6e6e6;
  border-top: 0px;
  padding: 10px 20px;
  position: relative;
  overflow: hidden;
}

.equipe .titre .triangle {
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 0 0 2000px 800px;
  border-color: transparent transparent #b474c2 transparent;
  position: absolute;
  top: -650px;
  right: 0px;
  z-index: 1;
}

.equipe .titre h2 {
  font-family: roboto;
  font-style: italic;
  color: #b474c2;
  text-transform: lowercase;
  margin: 0;
  position: relative;
  z-index: 2;
}

.pokemons {
  background: white;
  border: 1px solid #e6e6e6;
  padding: 20px;
  margin-top: 10px;
  position: relative;
}

.pokemons .infopoke {
  position: relative;
  width: 23%;
  float: right;
  text-align: right;
}

.pokemons .infopoke .icopoke {
  border-radius: 100px;
  background: #f8f8f8;
  padding: 5px;
  border: 1px solid #e6e6e6;
  position: relative;
  z-index: 2;
  margin-left: 13%;
}

.pokemons .infopoke .nv {
  text-transform: uppercase;
  font-size: 14px;
  font-family: roboto;
  background: #f8f8f8;
  border-radius: 100px;
  padding: 10px;
  width: 20px;
  z-index: 1;
  position: absolute;
  top: 23px;
  left: 4px;
}

.pokemons .infopoke .nvc {
  text-transform: uppercase;
  font-size: 16px;
  font-family: roboto;
  background: #b474c2;
  border-radius: 100px;
  padding: 10px;
  width: 20px;
  color: white;
  z-index: 3;
  position: absolute;
  top: 50px;
  left: 18px;
}

.pokemons .infopoke .chroma {
  text-transform: uppercase;
  font-size: 14px;
  font-family: roboto;
  background: #e9e9e9;
  border-radius: 100px;
  padding: 8px;
  width: 12px;
  z-index: 4;
  position: absolute;
  top: 77px;
  left: 40px;
  height: 14px;
  padding-top: 6px;
}

.pokemons .chroma i.display {
  color: #e9e9e9;
}

.pokemons .descripoke {
  width: 20%;
  float: left;
  margin-left: 5%;
}

.pokemons .descripoke span {
  display: block;
  border-bottom: 1px solid #e6e6e6;
  text-transform: uppercase;
  font-size: 9px;
  font-family: roboto;
  text-align: right;
  padding: 5.5px;
}

.pokemons .descripoke span i {
  color: #b474c2;
  font-size: 12px;
  margin-left: 5%;
}

.pokemons .capa {
  width: 47%;
  float: left;
  background: #f8f8f8;
  text-transform: uppercase;
  font-size: 9px;
  font-family: roboto;
  margin-top: 5px;
  height: 95px;
  overflow: auto;
  padding: 5px;
}

.pokemons .capa img {
  position: relative;
  bottom: -2px;
  margin-right: 5px;
}

.pokemons .poke h3 {
  position: absolute;
  top: -76px;
  right: 25px;
  font-size: 25px;
  z-index: 3;
  font-family: roboto;
  font-style: italic;
  color: #f8f8f8;
  text-transform: lowercase;
}

.contenu_onglets {
  text-transform: uppercase;
  font-size: 9px;
  font-family: roboto;
}

.pokemons .infopoke .types {
  z-index: 4;
  position: absolute;
  top: 95px;
  left: 60px;
}

.contenu_poke {
  display: none;
}

.onglets_poke {
  text-align: center;
  margin-top: 5px;
}

.poke_0 {
  opacity: 0.5;
}

.poke_1 {
  opacity: 1;
}

.capa2 {
  width: 50%;
  float: left;
}

.non {
  background: #e6e6e6 !important;
}

clear {
  clear: both;
}

.boitepc {
  border: 1px solid #a5a5a5;
  margin-top: 10px;
  background: white;
  width: 598px;
  height: 30px;
  text-align: left;
  clear: both;
  position: relative;
  top: 5px;
  bottom: 5px;
  padding-top: 5px;
}

.onglet {
  display: inline-block;
  cursor: pointer;
}
.onglet_0 {
}
.onglet_1 {
}
.contenu_onglet {
  display: none;
}

.objets {
  width: 193px;
  float: left;
}
.listobjets,
.listcap {
  text-align: left;
  text-transform: uppercase;
  font-size: 10px;
  margin-top: 5px;
  color: #4d4d4d;
  height: 158px;
  overflow: auto;
  margin-bottom: 10px;
}

.objets img,
.listcap img {
  width: 15px;
  position: relative;
  bottom: -2px;
}

.capacite {
  width: 185px;
  float: left;
  margin-right: 8px;
}

.talents {
  width: 150px;
  float: left;
}

.badge img {
  margin: 6.5px 0;
  width: 29px;
}

.badge {
  border: 1px solid #a5a5a5;
  width: 30px;
  float: right;
  margin-top: 10px;
}

.sacados {
  height: 190px;
  width: 537px;
  font-size: 12px;
  font-family: arial;
  margin: auto;
  padding: auto;
}

.atts,
.listalent {
  background: #f1f1f1;
  border: 1px solid #a5a5a5;
  text-align: left;
  font-size: 10px;
  font-family: arial;
  padding: 5px;
  margin: 10px 5px;
  color: #4d4d4d;
  height: 120px;
  overflow: auto;
  text-transform: uppercase;
}

.atts img {
  position: relative;
  bottom: -2px;
}

.clear {
  clear: both;
}
.list li span {
  float: right;
  color: #949494;
}

.pokemon {
  width: 125px;
  float: left;
  position: relative;
  left: -15px;
  margin-right: 50px;
}
.type {
  margin-top: 18px;
}

.info {
  width: 145px;
  float: left;
  margin-left: 15px;
}

.list li strong {
  text-transform: uppercase;
  text-align: left;
  float: left;
  font-size: 10px;
  color: #4d4d4d;
  font-family: arial;
}

.att {
  width: 165px;
  float: left;
}
.t-card {
  width: 600px;
  margin: 0 auto;
}

.equipe {
  border: 1px solid #a5a5a5;
  margin-top: 10px;
  background: white;
  width: 32px;
  float: left;
  margin-right: 5px;
  padding-top: 0.6px;
  height: 186px;
}

.equipe img {
  margin: 4px 0;
  width: 23px;
  display: block;
}

.talent {
  background: #f1f1f1;
  padding: 3px;
  font-size: 10px;
  line-height: 11px;
  height: 48px;
  text-align: center;
  overflow: auto;
  margin: 0 12px;
  color: #949494;
}

.list {
  margin: 0;
  padding: 0;
  margin-top: 10px;
  display: block;
}
.list li {
  list-style: none;
  font-size: 12px;
  border-bottom: 1px solid #aeaeae;
  margin: 5px 12px;
}

h1 {
  font-family: "Oswald", sans-serif;
  font-size: 22px;
  text-transform: uppercase;
  color: #7e7e7e;
  font-weight: 700;
  margin: 0;
  line-height: 20px;
}

h3 {
  font-family: arial;
  font-size: 10px;
  text-transform: uppercase;
  color: #7e7e7e;
  margin: 0;
}

.listpoke {
  border: 1px solid #a5a5a5;
  padding: 10px;
  margin-top: 10px;
  background: url("https://www.zupimages.net/up/17/11/rdnt.png") no-repeat white;
  height: 167px;
  width: 500px;
  float: right;
  background-position: -11px 0px;
}

.name {
  background: black;
  color: white;
  text-transform: uppercase;
  font-family: cousine;
  font-size: 12px;
  padding-top: 2px;
}

.legend {
  font-family: cousine;
  font-size: 8px;
  text-transform: uppercase;
  margin-top: 4px;
}

.relation {
  width: 360px;
  float: left;
  margin-top: 20px;
}

.avatar {
  width: 50px;
  border: 10px solid;
  float: left;
}

.link {
  background: white;
  width: 431px;
  padding: 10px 30px;
}

.border {
  border: 1px solid #a5a5a5;
  width: 600px;
  margin-top: 10px;
}

.syd {
  width: 580px;
  height: 250px;
  background: #fefefe;
  overflow: hidden;
  border: solid 10px #fff;
}

.syd .box1 {
  width: 200px;
  height: 250px;
  float: left;
  background: #f1f1f1;
}

.syd .box2 {
  width: 380px;
  height: 250px;
  float: right;
  overflow: hidden;
}

.syd .right {
  width: 380px;
  height: 250px;
  transition: 2s;
}

.syd .left {
  margin-right: -60px;
  margin-left: 20px;
  height: 250px;
  position: relative;
  z-index: 20;
  padding-top: 100px;
  font: 8px cousine;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: #505050;
  opacity: 1;
  transition: 0.5s;
  transition-delay: 1.2s;
}

.syd .left b {
  color: #b0b4ce; /*** ACCENT ***/
}

.syd .left one {
  background: #fff;
  float: right;
  padding: 4px 15px 2px 15px;
  text-align: right;
  box-shadow: 1px 1px 1px #b6b6b6;
  transition: 0.5s;
  transition-delay: 0.6s;
}

.syd .left clear {
  display: block;
  clear: both;
  height: 10px;
}

.syd .text {
  width: 180px;
  height: 230px;
  overflow: auto;
  font: 10px/11px roboto;
  clear: both;
  text-align: justify;
  position: relative;
  float: left;
  z-index: 200;
  padding: 10px;
  background: #f1f1f1;
  transition: 0.6s;
  transition-delay: 0s;
  opacity: 0.2;
  color: #525252;
}

.syd .text::-webkit-scrollbar {
  background: #fff;
  width: 5px;
  border: solid 2px #f8f8f8;
}

.syd .text::-webkit-scrollbar-thumb {
  border-radius: 5px;
  background: #d9d9d9;
}

.syd:hover .left {
  padding-top: 200px;
  opacity: 0.9;
  transition: 0.5s;
  transition-delay: 0s;
}

.syd:hover .left one {
  margin-right: -170px;
  transition: 0.5s;
  transition-delay: 0.6s;
}

.syd:hover .right {
  -webkit-filter: grayscale(100%);
  filter: grayscale(100%);
}

.syd:hover .text {
  margin: -250px 0 0 0px;
  transition: 0.8s;
  transition-delay: 1s;
  opacity: 1;
}
</style>
