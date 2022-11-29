<template>
   

    <div class="reservations" id="reservations">
        <h2>Кабинет пользователя</h2>
        <a href="#" class="btn btn-success" @click="DialogShow">Add product</a>
        <MyDialog v-model:show="DialogVisible">
            <form>
                <FormButton></FormButton>
            </form>
        </MyDialog>
    </div>
</template>
<style>
.reservations {
    font-size: x-large;
    height: 600px;
    background: rgb(216, 179, 179);
}
</style>
<script>
import { ref } from "vue";
export default {
    name: "reservationsBody",
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