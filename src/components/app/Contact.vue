<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col cols="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Contact</v-subheader>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
            </v-col>
            <v-col cols="12" lg="6" md="6" sm="6">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3964.514772053435!2d106.82123381477041!3d-6.456268395329211!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69eb16abf7f6b3%3A0x1ad6867781a0772e!2sPT%20NIRTARA!5e0!3m2!1sid!2sid!4v1639798768162!5m2!1sid!2sid" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
            </v-col>
            <v-col cols="12" lg="6" md="6" sm="6">
                 <v-form ref="form" v-model="valid" lazy-validation>
                    <v-text-field v-model="name" label="Name" required ></v-text-field>
                    <v-text-field v-model="email" label="Email" required ></v-text-field>
                    <v-textarea v-model="bio" color="teal" >
                        <template v-slot:label>
                            <div> Message </div>
                        </template>
                    </v-textarea>
                    <v-btn color="blue" dark class="mr-4" > Send </v-btn>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            valid:'',
            name: '',
            email: '',
            bio: ''
        }
    }
}
</script>