<template>
  <section id="about">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2">Descarga nuestro menu
              <v-btn
                class="ma-2"
                color="indigo"
                dark
                href="https://bit.ly/3fvCvNC"
                target="_blank"
                >
                <v-icon dark>
                  mdi-cloud-upload
                </v-icon>
              </v-btn>
              </h1>
              
            </v-col>
            <v-col cols="12" md="7">
              <h1 class="font-weight-light display-2">Lo que nos define</h1>
              <h1 class="font-weight-light display-1 mb-3">
                Lo que nos definie!
              </h1>
              <v-row>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icon1.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    El mejor precio por un producto con la mejor calidad en el mercado,con una variedad de 50 sabores.
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icon2.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    Cientos de clientes que avalan nuestro compromiso al tener un producto que está por encima de la competencia
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icon3.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    Sabores y texturas fuera de este mundo, que te cautivaran desde el primer momento
                  </p>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12" md="5" class="d-none d-md-flex">
              <v-img
                src="@/assets/img/ima.png"
                class="d-block ml-auto mr-auto"
                max-width="400px"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#about {
  background-color: #f4f7f5;
}
</style>
