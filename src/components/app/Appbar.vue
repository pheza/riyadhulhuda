<template>
    <div>
        <v-app-bar
            app
            color="white"
            light
            elevation="6"
            elevate-on-scroll
        >
            <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-list-item two-line>
                <img class="hidden-md-and-down" src="../../assets/logopprdh.png"  width="56" >
                <v-list-item-content class="ml-2">
                    <v-list-item-title class="hidden-md-and-down" >Pondok Pesantren</v-list-item-title>
                    <v-list-item-title class=" blue--text font-weight-bold">RIYADHUL HUDA</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
            <v-spacer/>
            <v-list class="d-flex align-center">
                <v-list-item-group v-model="group" class="d-flex" active-class="deep-purple--text text--accent-4" >
                    <v-list-item class="hidden-sm-and-down"  link  @click="$vuetify.goTo('#beranda')">
                        <v-list-item-title>Beranda</v-list-item-title>
                    </v-list-item>
                    <v-list-item class="hidden-sm-and-down" link  @click="$vuetify.goTo('#selayang-pandang')">
                        <v-list-item-title>Selayang Pandang</v-list-item-title>
                    </v-list-item>
                    <v-dialog v-model="dialog" content-class="test"  hide-overlay >
                        <template v-slot:activator="{ on, attrs }">
                             <v-list-item
                                v-bind="attrs"
                                v-on="on"
                                class="hidden-sm-and-down">
                                <v-list-item-title > Pesantren </v-list-item-title>
                                <v-icon color="blue" >mdi-chevron-down</v-icon>
                            </v-list-item>
                        </template>
                            <v-col lg="12" class="px-0 py-0">
                                <v-card class="d-flex">
                                    <v-col lg="6" style="padding-bottom: 0px;padding-right: 0px;padding-top: 0px;padding-left: 0px;">
                                        <div class="py-10 px-10 mx-0 my-0" >
                                            <h3 class="my-2 ml-6">YPI RIYADHUL HUDA</h3>
                                            <v-row >
                                                <v-col  v-for="(n,i) in pesantrens" :key="i">
                                                    <v-list-item  two-line>
                                                        <v-btn class="mx-2" fab dark small :color="n.color" >
                                                            <v-icon dark>{{n.icon}}</v-icon>
                                                        </v-btn>
                                                        <v-list-item-content class="ml-3">
                                                            <v-list-item-title class=" font-weight-bold" >{{n.title}}</v-list-item-title>
                                                            <v-list-item-title class="gray--text">Alumni</v-list-item-title>
                                                        </v-list-item-content>
                                                    </v-list-item>
                                                </v-col>
                                            </v-row>
                                        </div>
                                    </v-col>
                                    <v-divider vertical></v-divider>
                                    <v-col lg="6" style="padding-bottom: 0px;padding-right: 0px;padding-top: 0px;padding-left: 0px;">
                                        <div class="py-10 px-10 mx-0 my-0" >
                                            <h3 class="my-2 ml-6">KANAL ALUMNI</h3>
                                            <v-row >
                                                <v-col cols="6" v-for="(a, i) in alumni" :key="i">
                                                    <v-list-item  two-line>
                                                        <v-btn class="mx-2" fab dark small :color="a.color" >
                                                            <v-icon dark>{{a.icon}}</v-icon>
                                                        </v-btn>
                                                        <v-list-item-content class="ml-3">
                                                            <v-list-item-title class=" font-weight-bold" >{{a.title}}</v-list-item-title>
                                                            <v-list-item-title class="gray--text">Alumni</v-list-item-title>
                                                        </v-list-item-content>
                                                    </v-list-item>
                                                </v-col>
                                            </v-row>
                                        </div>
                                    </v-col>
                                </v-card>
                            </v-col>
                    </v-dialog>
                    <v-list-item class="hidden-sm-and-down" link  @click="$vuetify.goTo('#gallery')">
                        <v-list-item-title>Gallery</v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
                <v-btn class="" text>
                    <v-icon>mdi-magnify</v-icon>
                </v-btn>
                <v-btn class="hidden-sm-and-down" outlined color="blue">
                    Pendaftaran Santri Baru
                </v-btn>
            </v-list>
        </v-app-bar>
        <v-navigation-drawer v-model="drawer" app>
             <template v-slot:prepend>
                <v-list-item two-line>
                    <img src="../../assets/logopprdh.png" width="56" >
                <v-list-item-content class="ml-2">
                    <v-list-item-title >Pondok Pesantren</v-list-item-title>
                    <v-list-item-title class=" blue--text font-weight-bold">RIYADHUL HUDA</v-list-item-title>
                </v-list-item-content>
                </v-list-item>
            </template>
            <v-divider></v-divider>
            <v-list nav dense >
                <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4" >
                    <v-list-item link v-for="(menu, ind) in menus" :key="ind" @click="$vuetify.goTo(menu.route)">
                         <v-list-item-icon>
                            <v-icon color="blue">{{ menu.icon }}</v-icon>
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>{{menu.title}}</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                    <v-divider class="my-2"></v-divider>
                    <v-btn dark color="blue">
                        Form Pendaftaran
                    </v-btn>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>

<script>
export default {
    name: 'Appbar',
    data() {
        return {
            dialog: false,
            menus: [
                {icon: 'mdi-home', title: 'Beranda', route: '#beranda'},
                {icon: 'mdi-home', title: 'Selayang Pandang', route: '#selayang-pandang'},
                {icon: 'mdi-briefcase', title: 'Pesantren', route: '#portfolio'},
                {icon: 'mdi-poll', title: 'Pendidikan', route: '#project'},
                {icon: 'mdi-view-gallery', title: 'Gallery', route: '#gallery'},
                {icon: 'mdi-information-outline', title: 'Berita', route: '#about-us'},
                {icon: 'mdi-phone', title: 'Kontak', route: '#contact'},
            ],
            items: [
                { title: 'Click Me' },
                { title: 'Click Me' },
                { title: 'Click Me' },
                { title: 'Click Me 2' },
            ],
            pesantrens: [
                {icon: 'mdi-home', title: 'Pondok Pesantren', route: '#pondok-pesantren', color: 'blue'},
                {icon: 'mdi-home', title: 'TKQ & TPQ', route: '#tkq-tpq', color: 'success'},
                {icon: 'mdi-briefcase', title: 'SMP PLUS', route: '#smp-plus', color: 'red'},
                {icon: 'mdi-poll', title: 'SMK PLUS', route: '#smk-plus', color: 'orange'},
                {icon: 'mdi-view-gallery', title: 'MAJELIS TA`LIM', route: '#majelis-taklim', color: 'indigo'},
            ],
            alumni: [
                {icon: 'mdi-home', title: 'Info Alumni', route: '#info-alumni', color: 'blue'},
                {icon: 'mdi-home', title: 'Jadwal Alumni', route: '#jadwal-alumni', color: 'success'},
                {icon: 'mdi-briefcase', title: 'Kegiatan Alumni', route: '#kegiatan-alumni', color: 'red'},
                {icon: 'mdi-poll', title: 'Program Alumni', route: '#program-alumni', color: 'orange'},
                {icon: 'mdi-view-gallery', title: 'Bansos', route: '#bansos', color: 'indigo'},
            ],

      drawer: false,
      group: null,
        }
    },
    watch: {
      group () {
        this.drawer = false
      },
    }
}
</script>

<style>
    .v-toolbar__title{
        font-size: 32px;
        font-weight: 700;
    }
    .test {
        position: absolute;
        top: 44px;
    }
</style>