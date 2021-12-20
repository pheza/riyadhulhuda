<template>
    <v-container class="pt-16">
        <v-row>
            <v-col cols="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Selayang Pandang</v-subheader>
            </v-col>
            <v-col cols="12" lg="6" md="6" sm="6">
                <v-card class=" pa-1">
                    <v-list-item two-line>
                        <img src="../../assets/kh.png" width="56" >
                    <v-list-item-content class="ml-2">
                        <v-list-item-title >Pimpinan Pondok Pesantren Riyadhul Huda</v-list-item-title>
                        <v-list-item-title class=" black--text font-weight-bold">KH. Obih Baihaqi</v-list-item-title>
                    </v-list-item-content>
                    </v-list-item>
                    <v-card-subtitle class="text-justify">
                        YPI RIYADHUL HUDA di dirikan oleh Al Mukarom  Kh. Obih Baihaqi pada juni 1996.Salah satu cabang dari Ponpes Miftahul Huda Manonjaya ini berdiri diatas lahan lebih dari 200m2. Yayasan pendidikan islam ini selain berupaya mencetak para peserta didik nya dengan akhlak yang mulia dan mendapat ilmu yang beermanfaat.demi tercapainya tujuan yang mulia tersebut, lembaga ini selalu memiliki strategi luar biasa dalam bentuk kegiatan dan pembinaan selama 24 jam kepada para santri-nya supaya memiliki kecerdasan intelektual dan emosional yang luar biasa pula, serta memiliki spiritual sehingga lembaga ini memiliki program - program dalam bentuk ibadah berjamaah setiap waktu seperti shalat fardhu berjamaah awal waktu, shalat tahajjud & dhuha.Riyadhoh Qolbu dan Tadarus Al-qur'an. Tentunya semua program tersebut hanya sebagian kecil dari program unggulan lainnya yang telah di rancang oleh al mukarom beserta para pengurus dan jajarannya.
                    </v-card-subtitle>
                </v-card>
            </v-col>
            <v-col lg="6" data-aos="fade-left">
                 <v-card class=" pa-1">
                    <img width="100%" src="../../assets/ponpes.png" data-aos="fade-down">
                 </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'Hero',
    data() {
        return {
        }
    }
}
</script>
<style scoped>
    h2.intro-text {
        font-size: 32px;
        font-weight: bold;
        color: #444;
    }
    p.description {
        font-size: 19px;
        margin: 32px 0px;
        color: #444444ba;
    }
</style>