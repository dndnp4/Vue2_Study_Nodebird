<template>
    <v-app>
        <div>
            <v-toolbar dark color='green'>
                <v-toolbar-title>
                    <nuxt-link to="/">NodeBrid</nuxt-link>
                </v-toolbar-title>
                <v-spacer></v-spacer>
                    <v-text-field label="search" hide-details prepend-icon="mdi-magnify"></v-text-field> 
                <v-toolbar-items> 
                    <v-btn text nuxt to="/profile">
                        <div>priofile</div>
                    </v-btn>
                    <v-btn text nuxt to="/signup">
                        <div>signup</div>
                    </v-btn>
                </v-toolbar-items>
            </v-toolbar>
        </div>
    <v-row no-gutters>
        <v-col cols="12" md="4">
            <login-form></login-form>
        </v-col>
        <v-col cols="12" md="8">
            <nuxt/>
        </v-col>
    </v-row>
    </v-app>
</template>

<script>

import LoginForm from '~/components/LoginForm';

export default {
    components : {
        LoginForm
    },
    data() {
        return {
            
        };
    }
};
</script>

<style lang="scss" scoped>

</style>