<template>

    <div class="container">
        <div class="row">
            <div class="col-md-3"></div>
            <div class="col-md-6" v-if="mode == 'login'">
                <form>
                <h1 class="card__title">Login</h1>
                <br>
                <p>Vous n'avez pas encore de compte ? <span class="card__action" @click="createAccount()">Créer un compte</span></p>
                <div class="mb-3">
                    <input placeholder="Enter Email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                </div>
                <div class="mb-3">
                    <input placeholder="Enter Password" type="password" class="form-control" id="exampleInputPassword1">
                </div>
                <button type="submit" class="btn btn-primary">Connexion</button>
                </form>
            </div>

            <div class="col-md-6" v-else>
                <form>
                <h1 class="card__title">Create an account</h1>
                <br>
                <p>Vous avez déjà un compte ? <span class="card__action" @click="login()">Connectez vous !</span></p>
                <div class="mb-3">
                    <input placeholder="Enter Email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                </div>
                <div class="mb-3">
                    <input placeholder="Enter Pseudo" type="text" class="form-control" id="exampleInputPseudo1">
                </div>
                <div class="mb-3">
                    <input placeholder="Enter Phone" type="tel" class="form-control" id="exampleInputPhone1">
                </div>
                <div class="mb-3">
                    <input placeholder="Enter Password" type="password" class="form-control" id="exampleInputPassword1">
                </div>
                <button type="submit" class="btn btn-primary">Register</button>
                </form>
            </div>
            <div class="col-md-3"></div>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'Profile',

    data: () => {
        return {
            mode: 'login'
        }
    },

    methods: {
        createAccount() {
            this.mode = "create"
        },

        login() {
            this.mode = "login"
        }
    }
}
</script>

<style scoped>

form {
    background-color: #F0CF1E;
    padding: 50px 100px;
    border-radius: 50px;
}

form span {
    color: #5481F0;
    cursor: pointer;
}

</style>