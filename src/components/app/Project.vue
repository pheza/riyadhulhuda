<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col cols="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Media Santri</v-subheader>
                <p>Berita Terkini Dari Pondok Pesantren Riyadhul Huda</p>
            </v-col>
            <v-col cols="12" lg="4" md="4">
                <v-card 
                    class="mx-auto my-12"
                    max-width="374"
                    >
                    <iframe src="https://www.facebook.com/plugins/video.php?height=476&href=https%3A%2F%2Fweb.facebook.com%2Friyadhulhuda96%2Fvideos%2F1042038686202231%2F&show_text=false&width=267&t=0" width="367" height="380" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
                        <v-card-title>Ibnu Atho'illah</v-card-title>
                        <v-card-text>
                            <div>
                                Telah Melakukan Setoran hafalan Kitab Shorof dengan Durasi 30 menit 16 Detik
                            </div>
                        </v-card-text>
                        <v-divider class="mx-4"></v-divider>
                        <v-card-actions>
                             <v-btn outlined>
                                <v-icon color="blue" right>mdi-thumb-up</v-icon>
                                120
                            </v-btn>
                        </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'Project',
    data() {
        return {
        
        }
    }
}
</script>