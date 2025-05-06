<template>
    <div class="card">
        <div v-if="$slots.header" class="card-header">
            <slot name="header" header-message="헤더 메시지!!!">#header</slot>
        </div>
        <div v-if="$slots.default" class="card-body">
            <slot :child-message="childMessage" hello-message="안녕하세요.">#body</slot>
        </div>
        <div v-if="$slots.footer" class="card-footer text-body-secondary">
            <slot name="footer" footer-message="푸터 메시지!!!">#footer</slot>
        </div>
    </div>
</template>

<script>
import { ref } from 'vue';

export default {
    setup () {
        const childMessage = ref('자식 메시지입니다.!')
        return {
            childMessage
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
