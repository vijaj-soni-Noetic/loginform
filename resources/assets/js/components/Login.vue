<template>
    <div class="container">
        <div class="text-center" style="padding:50px 0">
            <div class="logo">login</div>
            <!-- Main Form -->
            <div class="login-form-1">
                <form class="text-left">
                    <div class="login-form-main-message"></div>
                    <div class="main-login-form">
                        <div class="login-group">
                            <div class="form-group">
                                <label for="lg_username" class="sr-only">Username</label>
                                <input type="text" class="form-control" id="lg_username" name="lg_username" v-model="username" placeholder="username">
                            </div>
                            <div class="form-group">
                                <label for="lg_password" class="sr-only">Password</label>
                                <input type="password" class="form-control" id="lg_password" name="lg_password" v-model="password" placeholder="password">
                            </div>
                            <div class="form-group login-group-checkbox">
                                <input type="checkbox" id="lg_remember" v-model="remember" name="lg_remember">
                                <label for="lg_remember">remember</label>
                            </div>
                        </div>
                        <button type="submit" class="login-button" v-on:click.prevent="login"><i class="fa fa-chevron-right"></i></button>
                    </div>
                    <div class="etc-login-form">
                        <p>forgot your password? <a href="#">click here</a></p>
                        <p>new user? <a href="#">create new account</a></p>
                    </div>
                </form>
            </div>
            <!-- end:Main Form -->
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                username: '',
                password: '',
                remember: ''
            }
        },
        methods: {
            login: function () {
                const postData = {
                    username: this.username,
                    password: this.password,
                }
                console.log(postData)
            }
        }
    }
</script>