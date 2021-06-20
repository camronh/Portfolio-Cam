<template>
  <div>
    <v-app-bar flat color="transparent">
      <v-spacer></v-spacer>
      <AvatarMenu />
    </v-app-bar>
    <br />
    <v-container fluid pa-0>
      <v-row align="center" justify="center" dense>
        <v-col
          cols="12"
          lg="8"
          md="8"
          class="d-flex flex-column justify-center align-center"
        >
          <v-card width="100%">
            <v-card-title>
              <h1>
                Brazy Proxies
              </h1>
            </v-card-title>
            <v-card-text>
              <h3>
                A High-Speed VPN company focused on the Sneaker Arbitrage
                market, that I started in 2016.
              </h3>
            </v-card-text>
            <v-card-text>
              <v-carousel
                cycle
                height="600"
                hide-delimiters
                show-arrows-on-hover
              >
                <v-carousel-item v-for="(slide, i) in slides" :key="i">
                  <v-sheet :color="colors[i]" height="100%">
                    <v-row class="fill-height" align="center" justify="center">
                      <div class="text-h2">{{ slide }} Slide</div>
                    </v-row>
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>
            </v-card-text>
            <v-card-title>
              <h2>
                Description:
              </h2>
            </v-card-title>
            <v-card-text>
              <h3>
                In the Sneaker Arbitrage market, users race to get limited
                products on the day release days. To increase their odds, some
                users use Sneaker Bots which require VPNs for identity
                obfuscation. For these users, speed is the most important factor
                in choosing a VPN Provider.
              </h3>
            </v-card-text>
            <br />
            <v-divider></v-divider>
            <br />

            <v-card-title>
              <h2>
                Technical Sheet
              </h2>
            </v-card-title>
            <v-card-text>
              <h3>
                Technologies that I got involved with during this project
              </h3>
              <br />

              <v-chip-group column>
                <v-chip
                  v-for="skill of skills"
                  :key="skill"
                  outlined
                  color="primary"
                  disabled
                >
                  {{ skill }}
                </v-chip>
              </v-chip-group>

              <br />
              <v-divider></v-divider>
              <br />
              <v-card-title>
                Brazy Proxies consists of 3 parts
              </v-card-title>

              <v-card-text>
                <v-expansion-panels flat v-model="panel">
                  <v-expansion-panel>
                    <v-expansion-panel-header>
                      <h3>
                        Proxy Servers
                      </h3>
                    </v-expansion-panel-header>
                    <v-expansion-panel-content>
                      <v-container>
                        <v-row no-gutters align="center" justify="center">
                          <v-col cols="12" sm="6" md="8">
                            <v-card class="pa-2" tile flat>
                              <v-card-text>
                                The VPNs offered in the Brazy Proxies service
                                are hosted on a cluster of dedicated Linux
                                servers from multiple cloud providers. We own
                                the IPs and the servers and are responsible for
                                the uptime and operations of these Squid servers
                              </v-card-text>
                            </v-card>
                          </v-col>
                          <v-col cols="6" md="4">
                            <v-card class="pa-2" tile>
                              <v-sheet color="green" height="200px">
                                <v-row
                                  class="fill-height"
                                  align="center"
                                  justify="center"
                                >
                                  <div class="text-h2">IMG</div>
                                </v-row>
                              </v-sheet>
                            </v-card>
                          </v-col>
                        </v-row>
                      </v-container>
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                  <v-expansion-panel>
                    <v-expansion-panel-header>
                      <h3>
                        Admin Dashboard
                      </h3>
                    </v-expansion-panel-header>
                    <v-expansion-panel-content>
                      <v-container>
                        <v-row no-gutters align="center" justify="center">
                          <v-col cols="6" md="4">
                            <v-card class="pa-2" tile>
                              <v-sheet color="green" height="200px">
                                <v-row
                                  class="fill-height"
                                  align="center"
                                  justify="center"
                                >
                                  <div class="text-h2">IMG</div>
                                </v-row>
                              </v-sheet>
                            </v-card>
                          </v-col>
                          <v-col cols="12" sm="6" md="8">
                            <v-card class="pa-2" tile flat>
                              Lorem ipsum dolor sit amet, consectetur adipiscing
                              elit, sed do eiusmod tempor incididunt ut labore
                              et dolore magna aliqua. Ut enim ad minim veniam,
                              quis nostrud exercitation ullamco laboris nisi ut
                              aliquip ex ea commodo consequat.
                            </v-card>
                          </v-col>
                        </v-row>
                      </v-container>
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                  <v-expansion-panel>
                    <v-expansion-panel-header>
                      <h3>
                        User Interface
                      </h3>
                    </v-expansion-panel-header>
                    <v-expansion-panel-content>
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                      sed do eiusmod tempor incididunt ut labore et dolore magna
                      aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                      ullamco laboris nisi ut aliquip ex ea commodo consequat.
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                </v-expansion-panels>
              </v-card-text>
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn text color="grey" link to="/portfolio">
                Portfolio
              </v-btn>
              <v-btn text color="grey">
                Contact Me
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import AvatarMenu from "../components/AvatarMenu";
export default {
  components: {
    AvatarMenu,
  },
  data() {
    return {
      showMenu: false,
      panel: 0,
      colors: [
        "indigo",
        "warning",
        "pink darken-2",
        "red lighten-1",
        "deep-purple accent-4",
      ],
      slides: ["First", "Second", "Third", "Fourth", "Fifth"],
      skills: ["NodeJS", "Lambda", "API Gateway", "CI/CD", "VueJS", "Linux"],
    };
  },
};
</script>
