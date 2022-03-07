<template>
    <div>
    
        <v-container>
    
            <v-card>
    
                <v-container>
    
                    <v-subheader>signup</v-subheader>
    
                    <v-form v-model="valid" @submit.prevent="onSubmitForm">
    
                        <v-text-field label='email' type='email' v-model="email" :rules="emailRules" required></v-text-field>
    
                        <v-text-field label='password' type='password' v-model="password" :rules="passwordRules" required></v-text-field>
    
                        <v-text-field label='refeat' type='password' v-model="passwordCheck" :rules="passwordCheckRules" required></v-text-field>
    
                        <v-text-field label='nickname' type='nickname' v-model="nickname" :rules="nicknameRules" required></v-text-field>
    
                        <v-checkbox required label='hello world' v-model="terms"></v-checkbox>
    
                        <v-btn color='green' type='submit'>signup</v-btn>
    
                    </v-form>
                </v-container>
    
            </v-card>
    
        </v-container>
    
    </div>
</template>

<script>
export default {

    data() {
        return {
            valid: false,
            email: '',
            password: '',
            passwordCheck: '',
            nickname: '',
            terms: false,
            emailRules: [
                v => !!v || '이메일은 필수입니다.',
                v => /.+@.+/.test(v) || '이메일이 유효하지 않습니다.',
            ],
            nicknameRules: [
                v => !!v || '닉네임은 필수입니다.',
            ],
            passwordRules: [
                v => !!v || '비밀번호는 필수입니다.',
            ],
            passwordCheckRules: [
                v => !!v || '비밀번호 확인은 필수입니다.',
                v => v === this.password || '비밀번호가 일치하지 않습니다.',
            ],
        };
    },
    head() {
        return {
            title: 'signup'
        }
    }
};
</script>

<style lang="scss" scoped>

</style>