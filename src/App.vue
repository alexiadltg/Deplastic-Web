<template>
    <v-app>
        <v-app-bar app dark color="green">
            <v-img
                lazy-src="https://cdn.discordapp.com/attachments/1032596789473333298/1035162795563561040/unknown.png"
                max-height="50"
                max-width="50"
                src="https://cdn.discordapp.com/attachments/1032596789473333298/1035162795563561040/unknown.png"
            >
            </v-img>
            <v-toolbar-title>Deplastic</v-toolbar-title>
            <v-spacer> </v-spacer>
            <v-btn text rounded>Home</v-btn>
            <v-btn text rounded>Login</v-btn>
            <v-btn text rounded>About</v-btn>
            <v-btn text rounded>Contact us</v-btn>
        </v-app-bar>

        <v-content>
            <v-card width="500" class="mx-auto mt-9">
                <v-card-title>Login</v-card-title>

                <v-card-text>
                    <v-text-field label="Username" prepend-icon="mdi-account-circle"> </v-text-field>

                    <v-text-field
                        label="Password"
                        :type="showPassword ? `text` : `Password`"
                        prepend-icon="mdi-lock"
                        :append-icon="showPassword ? `mdi-eye` : `mdi-eye-off`"
                        @click:append="showPassword = !showPassword"
                    >
                    </v-text-field>
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                    <v-btn dark color="green">Login</v-btn>
                </v-card-actions>
            </v-card>
        </v-content>
    </v-app>
</template>

<script>
export default {
    data() {
        return {
            showPassword: false,
        };
    },
};
</script>
