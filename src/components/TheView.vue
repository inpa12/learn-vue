<template>
    <main>
<<<<<<< HEAD
        <div class="container py-4">
            <MyButton class="my-button" id="my-button" @click="sayHello"></MyButton>
            <LabelInput label="이름" data-id="id입니다."></LabelInput>
        </div>
    </main>
</template>

<script>
import MyButton from './MyButton.vue'
import LabelInput from './LabelInput.vue'

export default {
    components: {
        MyButton,
        LabelInput,
    },
    setup() {
        const sayHello = () => {
            alert('안녕하세요!')
        }
        return {
            sayHello,
        }
    },
}
=======
        <DynamicComponent></DynamicComponent>
    </main>
</template>

<script setup>
import DynamicComponent from './DynamicComponent.vue';
>>>>>>> c8dd4fa7301c38928b49119baeafb31fd9680e62
</script>

<style lang="scss" scoped>

</style>
