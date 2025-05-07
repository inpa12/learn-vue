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
<<<<<<< HEAD
    props: {
        type: {
            type: String,
            default: 'news',
            validator: (value) => {
                return ['news', 'notice'].includes(value)
            },
        },
        title: {
            type: String,
            required: true,
        },
        contents: {
            type: String,
            //required: true,
        },
        isLike: {
            type: Boolean,
            default: false,
        },
    },
    emits: ['toggleLike'],
    setup(props, context) {
        //console.log('props.title: ', props.title)
        const isLikeClass = computed(() => (props.isLike ? 'btn-danger' : 'btn-outline-danger'))
        const typeName = computed(() => (props.type === 'news' ? '뉴스' : '공지사항'))
        const toggleLike = () => {
            console.log('asdf')
            context.emit('toggleLike')
        }
=======
    setup () {
        const childMessage = ref('자식 메시지입니다.!')
>>>>>>> c8dd4fa7301c38928b49119baeafb31fd9680e62
        return {
            childMessage
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
