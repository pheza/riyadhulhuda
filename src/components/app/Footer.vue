<template>
    <v-footer dark >
        <v-col  lg="12">
            <v-row justify="center">
                <v-col lg="4" class="text-center">
                    <v-toolbar-title>Social Media</v-toolbar-title>
                    <v-card-text>
                        <v-btn v-for="icon in icons" :key="icon" class="mx-4" color="blue" icon >
                            <v-icon size="24px"> {{ icon }} </v-icon>
                        </v-btn>
                    </v-card-text>
                    <v-subheader>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum assumenda totam magnam iusto enim vero dolorum, rerum nam expedita ullam.</v-subheader>
                    <v-form class="mt-4">
                        <v-text-field label="Email" outlined dense />
                        <v-btn rounded color="blue" dark>Subscribe</v-btn>
                    </v-form>
                </v-col>
            </v-row>
            <div class="mt-10">
                <v-divider></v-divider>
                <v-subheader>
                    &copy; Copyright Riyadhul Huda All Rights Reserved {{ new Date().getFullYear() }}
                    <v-spacer></v-spacer>
                    <strong>Design By Aseptian Abdurohman</strong>
                </v-subheader>
            </div>
        </v-col>                               
  </v-footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return{
            icons: [
                'mdi-facebook',
                'mdi-twitter',
                'mdi-linkedin',
                'mdi-instagram',
            ],
        }
    }
}
</script>