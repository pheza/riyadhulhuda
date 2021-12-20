<template>
    <v-container>
        <v-row>
            <v-col cols="12" lg="6" md="6">
                <v-subheader class=" text-h4"> About Us</v-subheader>
                <p> Lorem ipsum dolor sit. Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum nesciunt voluptatibus possimus sit doloremque? Voluptate?</p>
                <v-list>
                    <v-list-item 
                    data-aos="fade-right"
                    data-aos-duration="3000"
                    >
                        <v-icon color="blue" class="mr-3">mdi-check-all</v-icon>
                        <v-list-item-subtitle>Lorem, ipsum dolor sit amet consectetur Lorem ipsum dolor sit amet.</v-list-item-subtitle>
                    </v-list-item>
                    <v-list-item 
                    data-aos="fade-up"
                    data-aos-duration="3000"
                    >
                        <v-icon color="blue" class="mr-3">mdi-check-all</v-icon>
                        <v-list-item-subtitle>Lorem, ipsum dolor sit amet consectetur </v-list-item-subtitle>
                    </v-list-item>
                    <v-list-item 
                    data-aos="fade-left"
                    data-aos-duration="3000"
                    >
                        <v-icon color="blue" class="mr-3">mdi-check-all</v-icon>
                        <v-list-item-subtitle>Lorem, ipsum dolor sit amet consectetur Lorem, ipsum dolor. </v-list-item-subtitle>
                    </v-list-item>
                </v-list>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quo consectetur repudiandae dolorem aut ullam optio cumque aliquam in alias perspiciatis! Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam vitae a enim modi praesentium, quis debitis in. Vero, id ratione.</p>
            </v-col>
            <v-col cols="12" lg="6" md="6">
                <img
                width="100%"
                src="../../assets/Aboutus.jpg" 
                data-aos="fade-left"
                data-aos-duration="3000"
                >
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'Aboutus',
    data() {
        return {
        }
    }
}
</script>