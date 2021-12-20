<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col cols="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Gallery</v-subheader>
            </v-col>
            <v-col cols="12">
                <div class="text-center ">
                    <v-chip
                        class="mx-3 mt-2"
                        v-for="(chip, i) in gallery" :key="i"
                        @click="active = `${chip.active}`"
                        :color="active === `${chip.active}` ? 'blue' : ''"
                        dark
                    >
                        {{chip.title}}
                    </v-chip>
                </div>
            </v-col>
            <slot v-if="active === 'smk'">
                <v-col cols="12" lg="3" md="3" sm="4" v-for="(s, i) in smk" :key="i">
                    <v-card :data-aos="s.aos" data-aos-duration="3000">
                        <v-img
                        :src="s.url"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                        >
                        <v-card-title>{{s.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
            <slot v-if="active === 'pesantren'">
                <v-col cols="12" lg="3" md="3" sm="4" v-for="(p, i) in pesantren" :key="i">
                    <v-card :data-aos="p.aos" data-aos-duration="3000">
                        <v-img
                        :src="p.url"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                        >
                        <v-card-title>{{p.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
            <slot v-if="active === 'alumni'">
                <v-col cols="12" lg="3" md="3" sm="4" v-for="(a, i) in alumni" :key="i">
                    <v-card :data-aos="a.aos" data-aos-duration="3000">
                        <v-img
                        :src="a.url"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                        >
                        <v-card-title>{{a.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
            <slot v-if="active === 'smp'">
                <v-col cols="12" lg="3" md="3" sm="4" v-for="(s, i) in smp" :key="i">
                    <v-card :data-aos="s.aos" data-aos-duration="3000">
                        <v-img
                        :src="s.url"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                        >
                        <v-card-title>{{s.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'Gallery',
    data() {
        return {
            show: true, 
            active:'smk',
            gallery : [
                {aos: 'fade-right', title: "Pesantren", active: 'pesantren',},
                {aos: 'fade-left', title: "SMK Plus", active: 'smk',},
                {aos: 'fade-up', title: "SMP Plus", active: 'smp',},
                // {aos: 'fade-left', title: "TKA Plus", active: 'tka',},
                // {aos: 'fade-up', title: "TPQ Plus", active: 'tpq',},
                {aos: 'fade-right', title: "Alumni", active: 'alumni',},
                
            ],
            smk: [
                {aos: 'fade-left',title: "SMK Plus", url: require('@/assets/smk/1.jpg') },
                {aos: 'fade-up',title: "SMK Plus", url: require('@/assets/smk/7.jpg') },
                {aos: 'fade-right',title: "SMK Plus", url: require('@/assets/smk/8.jpg') },
                {aos: 'fade-right',title: "SMK Plus", url: require('@/assets/smk/9.jpg') },
                {aos: 'fade-up',title: "SMK Plus", url: require('@/assets/smk/5.jpg') },
                {aos: 'fade-left',title: "SMK Plus", url: require('@/assets/smk/6.jpg') },
                {aos: 'fade-right',title: "SMK Plus", url: require('@/assets/smk/10.jpg') },
                {aos: 'fade-up',title: "SMK Plus", url: require('@/assets/smk/11.jpg') },
            ],
            pesantren: [
                {aos: 'fade-left',title: "Santri", url: require('@/assets/pesantren/1.jpg') },
                {aos: 'fade-up',title: "Santri", url: require('@/assets/pesantren/2.jpg') },
                {aos: 'fade-right',title: "Santri", url: require('@/assets/pesantren/3.jpg') },
                {aos: 'fade-up',title: "Santri", url: require('@/assets/pesantren/4.jpg') },
                {aos: 'fade-left',title: "Santri", url: require('@/assets/pesantren/5.jpg') },
                {aos: 'fade-up',title: "Santri", url: require('@/assets/pesantren/6.jpg') },
            ],
            smp: [
                {aos: 'fade-left',title: "Smp Plus", url: require('@/assets/smp/1.jpg') },
                {aos: 'fade-up',title: "Smp Plus", url: require('@/assets/smp/2.jpg') },
            ],
            alumni: [
                {aos: 'fade-left',title: "Alumni 2021", url: require('@/assets/alumni/1.jpg') },
                {aos: 'fade-up',title: "Alumni 2021", url: require('@/assets/alumni/2.jpg') },
                {aos: 'fade-right',title: "Alumni 2021", url: require('@/assets/alumni/3.jpg') },
                {aos: 'fade-up',title: "Alumni 2021", url: require('@/assets/alumni/4.jpg') },
                {aos: 'fade-left',title: "Alumni 2021", url: require('@/assets/alumni/5.jpg') },
                {aos: 'fade-up',title: "Alumni 2021", url: require('@/assets/alumni/6.jpg') },
            ],
        
        }
    }
}
</script>