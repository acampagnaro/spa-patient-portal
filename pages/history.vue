<template>
  <v-app id="inspire">
    <v-app-bar
      app
      shrink-on-scroll
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title class="font-weight-bold">Lista de Exames</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <v-col
            v-for="n in 6"
            :key="n"
            cols="auto"
          >
            <v-card
              class="mx-auto"
              width="500"
              dark
            >
              <v-app-bar
                flat
              >
                <v-toolbar-title class="title white--text pl-0">
                  <span class="headline">Ultrassonografia</span>
                </v-toolbar-title>

                <v-spacer></v-spacer>

                <v-menu
                  bottom
                  left
                >
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      dark
                      icon
                      v-bind="attrs"
                      v-on="on"
                    >
                      <v-icon>mdi-dots-vertical</v-icon>
                    </v-btn>
                  </template>

                  <v-list>
                    <v-list-item
                      v-for="(item, i) in items"
                      :key="i"
                    >
                      <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item>
                  </v-list>
                </v-menu>

              </v-app-bar>

              <v-card-text class="headline font-weight-bold">
                <v-icon
                  large
                  left
                >
                  mdi-calendar
                </v-icon>
                <span>Data do exame: 15/12/2020</span>
              </v-card-text>
              <v-card-text class="headline font-weight-bold">
                <v-icon
                  large
                  left
                >
                  mdi-doctor
                </v-icon>
                <span class="title">Profissional: Médico teste</span>
              </v-card-text>
              <v-card-text class="headline font-weight-bold">
                <v-icon
                  large
                  left
                >
                  mdi-doctor
                </v-icon>
                <span class="title">CRM: 12345-PR</span>
              </v-card-text>
              <v-card-text class="headline font-weight-bold">
                <v-icon
                  large
                  left
                >
                  mdi-flag
                </v-icon>
                <span class="title">Status: Em Andamento</span>
              </v-card-text>

              <v-card-actions>
                <v-list-item class="grow">
                  <v-list-item-avatar color="grey darken-3">
                    <v-img
                      class="elevation-6"
                      alt=""
                      src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                    ></v-img>
                  </v-list-item-avatar>

                  <v-list-item-content>
                    <v-list-item-title>Claudio</v-list-item-title>
                  </v-list-item-content>

                  <v-row
                    align="center"
                    justify="end"
                  >
                    <v-icon class="mr-1">
                      mdi-printer
                    </v-icon>
                    <span class="subheading mr-2">Imprimir</span>
                    <span class="mr-1">·</span>
                    <v-icon class="mr-1">
                      mdi-share-variant
                    </v-icon>
                    <span class="subheading">Compartilhar</span>
                  </v-row>
                </v-list-item>
              </v-card-actions>

            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'Imprimir' },
      { title: 'Enviar' }
    ]
  })
}
</script>
