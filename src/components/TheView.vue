<template>
    <main>
        <div class="container py-4">
            <MyButton class="my-button" id="my-button" @click="sayHello"></MyButton>
            <LabelInput label="이름" data-id="id입니다."></LabelInput>
            <hr />
            <FancyButton>Click!!</FancyButton>
        </div>
    </main>
</template>

<script>
import MyButton from './MyButton.vue'
import LabelInput from './LabelInput.vue'
import FancyButton from './FancyButton.vue'

export default {
    components: {
        MyButton,
        LabelInput,
        FancyButton
    },
    setup() {
        const sayHello = () => {
           alert('안녕하세요!')
        }
        return {
            sayHello
        }
    },
}
</script>

<style lang="scss" scoped></style>
