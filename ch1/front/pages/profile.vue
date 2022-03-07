<template>
    <div>
        <v-container>
            <v-card style="margin-bottom: 20px">
                <v-container>
                    <v-subheader>my profile</v-subheader>
                    <v-form>
                        <v-text-field label='nickname' required></v-text-field>
                        <v-btn color='blue' type='submit'>rewrite</v-btn>
                    </v-form>
                </v-container>
            </v-card>
            <v-card style="margin-bottom: 20px">
                <v-container>
                    <v-subheader>following</v-subheader>
                    <follow-list></follow-list>
                </v-container>
            </v-card>
            <v-card style="margin-bottom: 20px">
                <v-container>
                    <v-subheader>follower</v-subheader>
                    <follow-list></follow-list>
                </v-container>
            </v-card>
        </v-container>
    </div>
</template>

<script>
import FollowList from '~/components/FollowList';

export default {
    components : {
        FollowList
    },
    data() {
        return {
            
        };
    },
    head() {
        return {
            title : 'profile'
        }
    }
};
</script>

<style lang="scss" scoped>

</style>