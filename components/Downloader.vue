<template>
  <v-card>
    <v-list>
      <v-list-item-group>
        <v-list-item v-for="it in downloadLinks"
                     :key="it.extension"
                     :href="it.link"
                     two-line>
          <v-list-item-icon>
            <v-icon>{{it.icon}}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>
              {{it.extension}}
            </v-list-item-title>
            <v-list-item-subtitle>
              {{it.system}}
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
    export default {
        name: "Downloader",
        data:function(){
            return {
                downloadLinks: [
                    {
                        extension: ".AppImage",
                        system: "Linux",
                        icon: "mdi-linux",
                        link: "https://github.com/Tallic/name-it/releases/download/v0.2.0/name-it-0.2.0.AppImage"
                    },
                    {
                        extension: ".exe",
                        system: "Windows x64",
                        icon: "mdi-microsoft-windows",
                        link: "https://github.com/Tallic/name-it/releases/download/v0.2.0/name-it-0.2.0.exe"
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>
