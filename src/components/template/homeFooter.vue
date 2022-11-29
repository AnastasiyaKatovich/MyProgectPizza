<template>
    <div>
    <footer>
        <div class="container">
            <div class="row text-white">
                <div class="col-lg-4 col-sm-12 text-center">
                    <h5>About Us</h5>
                    <img src="../../../public/image/Divider.png" alt="">
                    <h6>Lambda's new and exanded.</h6>
                    <a href="#" @click="DialogShow"> Сontacts here.</a>
                    <MyDialog v-model:show="DialogVisible">
                        <h5 class="slot-footer">
                        +375 5555555555
                            <br>+375 3333333333
                        
                        </h5>
                    </MyDialog>

                    <a href="#" @click="DialogShow1"> Сontacts here.</a>
                    <MyDialog v-model:show="DialogVisible1">
                        <h5 class="slot-footer">
                        +375 5555555555
                            <br>+375 3333333333
                        </h5>
                        
                    </MyDialog>
                </div>
                <div class="col-lg-4 col-sm-12 text-center">
                    <h5>About Us</h5>
                    <img src="../../../public/image/Divider.png" alt="">
                    <h6>Lambda's new and exanded. Chelsea location represents truly authentic Greek patisserie, featuring breakfasts of fresh crollssants and streming bowls of cafe. 
                        <br>Lambda the best restaurant in town.</h6>
                </div><div class="col-lg-4 col-sm-12 text-center">
                    <h5>About Us</h5>
                    <img src="../../../public/image/Divider.png" alt="">
                    <h6>Lambda's new and exanded.
                    Chelsea location represents truly authentic Greek patisserie, featuring breakfasts of fresh crollssants and streming bowls of cafe. 
                    <br>Lambda the best restaurant in town.</h6>
                </div>
            </div>
        </div>
    </footer>
</div>
</template>


<style scoped>
.slot-footer{
    color: black;
}
</style>
<script>
import { ref } from "vue";
export default {
    name: "reservationsBody",
    setup() {
        const DialogVisible1 = ref(false);
        const DialogShow1 = (e) => {
            e.preventDefault();
            console.log("test");
            DialogVisible1.value = true;
        }




        const DialogVisible = ref(false);
        const DialogShow = (e) => {
            e.preventDefault();
            console.log("test");
            DialogVisible.value = true;
        }
            return {
                DialogVisible,
                DialogShow,
                DialogVisible1,
                DialogShow1
            }
        }
        
    }
</script>