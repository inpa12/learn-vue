<template>
<<<<<<< HEAD
    <label>
        {{ label }}
        <input type="text" v-model="value" />
    </label>
</template>

<script>
import { computed } from 'vue'

export default {
    props: ['title', 'label'],
    emits: ['update:title'],
    setup(props, { emit }) {
        const value = computed({
            get() {
                return props.title
            },
            set(value) {
                emit('update:title', value)
            },
        })
        return {
            value,
        }
    },
}
=======
	<label>
		{{ label }}
		<input v-model="value" type="text" />
	</label>
</template>

<script>
import { computed } from '@vue/reactivity';

export default {
	props: ['title', 'label'],
	emits: ['update:title'],
	setup(props, { emit }) {
		const value = computed({
			get() {
				return props.title;
			},
			set(value) {
				emit('update:title', value);
			},
		});
		return { value };
	},
};
>>>>>>> c8dd4fa7301c38928b49119baeafb31fd9680e62
</script>

<style lang="scss" scoped></style>
