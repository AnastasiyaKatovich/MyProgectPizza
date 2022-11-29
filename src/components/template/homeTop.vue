<template>
    <div>
<header>
    <div class="container-fluid">
        <div class="row header-nav align-items-center">
            <div class="col-4 text-center">
                <h1 class="text-white">LAMBDA</h1>
            </div>
            <div class="col-7 text-center">
                <div class="row nav">
                        <div class="col-lg-2 col-sm-12">
                            <router-link to="/" class="nav text-white">
                                <h4>Home</h4>
                            </router-link>
                            <router-view/>
                        </div>
                        <div class="col-lg-2 col-sm-12">
                            <a href="/#about" class="nav text-white">
                                <h4>About</h4>
                            </a> 
                        </div>
                        <div class="col-lg-2 col-sm-12">
                            <a href="/#ingredients" class="nav text-white">
                                <h4>Ingredients</h4>
                            </a> 
                        </div>
                        <div class="col-lg-2 col-sm-12">
                            <a href="/#menu" class="nav text-white">
                                <h4>Menu</h4>
                            </a> 
                        </div>
                        <div class="col-lg-2 col-sm-12">
                            <a href="/#reviews" class="nav text-white">
                                <h4>Reviews</h4>
                            </a> 
                        </div>
                        <div class="col-lg-2 col-sm-12">
                            <a href="/#reservations" class="nav text-white">
                                <h4>Reservations</h4>
                            </a> 
                        </div>
                </div>
            </div>
            <div class="col-lg-1 col-sm-12 text-center">
                <a href="#" @click="DialogShow" class="nav text-white text-end">Sign IN</a>
                    <MyDialog v-model:show="DialogVisible">
                        <div>
                            <h3 class="">
                                Sign in
                            </h3>
                        </div>
                        <div>
                            <form>
                                <FormInput type="text" autofocus maxlength="10"></FormInput>
                            </form>
                        </div>
                        <div >
                            <form>
                                <FormInput type="text" autofocus maxlength="10"></FormInput>
                            </form>
                        </div>
                        <div>
                            Forgot Username/Password?
                        </div>
                        <div>
                            <form>
                                <FormButton nameValue="SIGN IN"></FormButton>
                            </form>
                        </div>
                        <div>
                            Don't have an account?
                        </div>
                        <div>
                            SIGN UP NOW
                        </div>
                    </MyDialog>
                <!--<a href="#" @click="DialogShow" class="nav text-white text-end">
                    <MyDialog v-model:show="DialogVisible">
                        <h5 class="slot-footer">
                        +375 5555555555
                            <br>+375 3333333333
                        
                        </h5>
                </MyDialog>
                <h4>
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-box-arrow-in-right" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M6 3.5a.5.5 0 0 1 .5-.5h8a.5.5 0 0 1 .5.5v9a.5.5 0 0 1-.5.5h-8a.5.5 0 0 1-.5-.5v-2a.5.5 0 0 0-1 0v2A1.5 1.5 0 0 0 6.5 14h8a1.5 1.5 0 0 0 1.5-1.5v-9A1.5 1.5 0 0 0 14.5 2h-8A1.5 1.5 0 0 0 5 3.5v2a.5.5 0 0 0 1 0v-2z"/>
                    <path fill-rule="evenodd" d="M11.854 8.354a.5.5 0 0 0 0-.708l-3-3a.5.5 0 1 0-.708.708L10.293 7.5H1.5a.5.5 0 0 0 0 1h8.793l-2.147 2.146a.5.5 0 0 0 .708.708l3-3z"/>
                    </svg>
                Sing in</h4>
                
                </a> -->
            </div>
            
        </div>
        <div class="row header-text text-center font-weight-bold text-white">
            <div class="col-12">
                <p class="h1"><strong>the right i
                    <br>for the right food
                </strong></p>
            </div>
        </div> 
        <div class="row header-divider">
            <div class="col-12">
                <img src="../../../public/image/Divider.png" class="rounded mx-auto d-block" alt="">
            </div>
        </div>
        <div class="row header-buttons">
            <div class="col-lg-4 col-sm-0">
            </div>
            <div class=" header-but col-lg-4 col-sm-12 text-center text-center text-uppercase">
                
                <a href="/table" class="button">BOOK A TABLE</a>
                <a href="/menu" class="button">SEE MENU</a>
                
            </div>
            <div class="col-lg-4 col-sm-0">
            </div>
        </div>
    </div>
</header>
</div>
</template>
<style scoped>
    .dialog_content{
        z-index: 100;
    }
    .header-but{
        display: flex;
        justify-content: space-around;
    }
    button{
        color:white;
        background-color: black;
        border: 1px solid white;
        opacity: 50%;
        width: 200px ;
        height:50px;
    }
    button:hover{
        color:white;
        border: 1px solid white;
        opacity: 100%;
    }
</style>
<script>
import { ref } from "vue";
export default {
    name: "homeTop",
    setup() {
        const DialogVisible = ref(false);
        const DialogShow = (e) => {
            e.preventDefault();
            console.log("test");
            DialogVisible.value = true;
        }
            return {
                DialogVisible,
                DialogShow
            }
        }
    }
</script>