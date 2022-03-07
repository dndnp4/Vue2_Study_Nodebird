<template>
    <v-container>
        <v-card>
            <v-form>
                <v-container>
                    <v-text-field label='email' type='email' required></v-text-field>
                    <v-text-field label='password' type='password' required></v-text-field>
                    <v-btn color='green' type='submit'>login</v-btn>
                    <v-btn nuxt to='/signup'>signup</v-btn>
                </v-container>
            </v-form>
        </v-card>
    </v-container>
</template>

<script>
export default {
    name: 'VueNodebirdLoginform',

    data() {
        return {
            
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>

</style>