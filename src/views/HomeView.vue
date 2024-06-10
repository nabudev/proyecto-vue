<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-white">Hola,</h1>
              <h1 class="text-white">Soy Nahuel Flores</h1>
              <span class="text-grey">Programador Back-End: Python, Django y MySQL</span><br />
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
              class="mt-16"
            >
              
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="i1.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg" style="background-color: black;">
                <v-img src="i2.png" max-height="300" class=""></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16"></h5>
              <div style="width: 120px">
                
              </div>
              <br>
              <br>
              <br>
              <h4 class="mt-n4">Desarrollo páginas web back-end</h4>
              <br>
              <p class="text-grey">
                Utilizo Python, Django y MySQL. Tengo experiencia en la creación de aplicaciones web escalables y eficientes, y he trabajado en diversos proyectos optimizando procesos y asegurando la integridad de los datos. Me apasiona mantenerme actualizado con las últimas tendencias tecnológicas para ofrecer siempre las mejores soluciones. Estoy disponible para colaborar en proyectos innovadores y desafiantes.
              </p>
              <br />
              
              
            </v-col>
          </v-row>
        </div>
      </v-col>

          <v-divider><!--Linea que separa el about me de mis proyectos--></v-divider>

      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <h1 class="mt-8">Proyectos realizados</h1>
          <!--espacio que separa el about me de los proyectos-->
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img :src="item.img" height="225px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          
        </div>
      </v-col>
      
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Información de Contacto</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">Argentina </span
              ><br />
              <v-btn
                icon="fas fa-phone-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">+549 3863 - 434058 </span> <br />
              
              <v-btn
                icon="fas fa-envelope"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">nabudev01@gmail.com </span> <br />
              
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Enviame tu mensaje</h1>
            <v-divider></v-divider>

            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Nombre"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Apellido"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Mensaje"
              persistent-hint
              variant="outlined"
            ></v-textarea>
            <v-btn color="#FBDF7E" class="mt-2">Enviar</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";
import NavBar from "../components/NavBar.vue";
import FooterView from "../components/FooterView.vue";

// Components
//import HelloWorld from '../components/HelloWorld.vue';

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "farmacia.png",
        },
        {
          img: "farmacia2.png",
        },
        {
          img: "mena.png",
        },
        {
          img: "alumnos2.jpg",
        },
        {
          img: "alumnos.jpg",
        },
        {
          img: "software.png",
        },
      ],
    };
  },
  components: {
    NavBar,
    FooterView
},
});


</script>
<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}

</style>
