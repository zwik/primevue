<script>
import BaseComponent from 'primevue/basecomponent';
import InputTextStyle from 'primevue/inputtext/style';

export default {
    name: 'BaseInputText',
    extends: BaseComponent,
    props: {
        modelValue: null,
        size: {
            type: String,
            default: null
        },
        invalid: {
            type: Boolean,
            default: false
        }
    },
    style: InputTextStyle,
    provide() {
        return {
            $parentInstance: this
        };
    }
};
</script>
