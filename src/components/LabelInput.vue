<template>
<<<<<<< HEAD
    <label class="form-label" id="child-id">
        {{ label }}
    </label>
    <input type="text" v-bind="$attrs" class="form-control" v-model="value" />
</template>

<script>
import { computed } from 'vue'

export default {
    props: ['modelValue', 'label'],
    emits: ['update:modelValue'],
    setup(props, { emit }) {
        const value = computed({
            get() {
                return props.modelValue
            },
            set(value) {
                emit('update:modelValue', value)
            },
        })
        return {
            value,
        }
    },
}
=======
	<label class="form-label" id="child-id">
		{{ label }}
	</label>
	<input v-model="value" v-bind="$attrs" type="text" class="form-control" />
</template>

<script>
import { computed } from '@vue/reactivity';

export default {
	props: ['modelValue', 'label'],
	emits: ['update:modelValue'],
	setup(props, { emit }) {
		const value = computed({
			get() {
				return props.modelValue;
			},
			set(value) {
				emit('update:modelValue', value);
			},
		});
		return { value };
	},
};
>>>>>>> c8dd4fa7301c38928b49119baeafb31fd9680e62
</script>

<style lang="scss" scoped></style>
