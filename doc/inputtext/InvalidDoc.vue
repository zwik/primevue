<template>
    <DocSectionText v-bind="$attrs">
        <p>Invalid state style is added using the <i>.p-invalid</i> class to indicate a failed validation.</p>
    </DocSectionText>
    <div class="card flex justify-content-center">
        <InputText v-model="value" invalid />
    </div>
    <DocSectionCode :code="code" />
</template>

<script>
export default {
    data() {
        return {
            value: null,
            code: {
                basic: `
<InputText v-model="value" invalid />
`,
                options: `
<template>
    <div class="card flex justify-content-center">
        <InputText v-model="value" invalid />
    </div>
</template>

<script>
export default {
    data() {
        return {
            value: null
        }
    }
}
<\/script>
`,
                composition: `
<template>
    <div class="card flex justify-content-center">
        <InputText v-model="value" invalid />
    </div>
</template>

<script setup>
import { ref } from 'vue';

const value = ref(null);
<\/script>
`
            }
        };
    }
};
</script>
