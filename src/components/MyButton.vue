<template>
<<<<<<< HEAD
    <div class="p-3 bg-danger">
        <!-- v-bind="$attrs" -->
        <button class="btn btn-primary" type="button" @click="sayHello">My Button</button>
    </div>
=======
	<div class="p-3 bg-danger">
		<button class="btn btn-primary" type="button" v-bind="$attrs">
			My Button
		</button>
		<!-- {{$attrs}} -->
	</div>
>>>>>>> c8dd4fa7301c38928b49119baeafb31fd9680e62
</template>

<script>
export default {
<<<<<<< HEAD
    // inheritAttrs: false,
    emits: ['click'],
    setup(props, { emit }) {
        // console.log('context.attrs: ', context.attrs)
        const sayHello = () => {
            emit('click')
        }
        return {
            sayHello,
        }
    },
}
=======
	inheritAttrs: false,
	setup(props, context) {
		// console.log('context.attrs: ', context.attrs);
		// console.log('class: ', context.attrs.class);
		// console.log('id: ', context.attrs.id);
		// console.log('onClick: ', context.attrs.onClick);
		// context.attrs.onClick();
		return {};
	},
};
>>>>>>> c8dd4fa7301c38928b49119baeafb31fd9680e62
</script>

<style lang="scss" scoped></style>
