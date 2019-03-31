<i-code-preview title="Custom Validator" markup="custom" link="https://github.com/inkline/inkline/blob/master/src/validators">
<i-form :schema="customValidatorForm">
    <i-form-group>
        <i-input :schema="customValidatorForm.input" v-model="customValidatorForm.input.value" placeholder="This field is custom validated. It needs to contain 'inkline'" />
    </i-form-group>
</i-form>
<template slot="html">

~~~html
<i-form :schema="form">
    <i-form-group>
        <i-input :schema="form.input" v-model="form.input.value" placeholder="This field is custom validated. It needs to contain 'inkline'." />
    </i-form-group>
</i-form>
~~~

</template>
<template slot="js">

~~~js
export default {
    data () {
        return {
            form: this.$form({
                input: {
                    validators: [
                        { rule: 'custom', validator: (v) => /inkline/.test(v) }
                    ]
                }
            })
        };
    }
}
~~~

</template>
<template slot="output">
<span class="_text-muted">// console.log(this.form);</span>
<pre>
<code>
{{ customValidatorForm | prettify }}
</code>
</pre>
</template>
</i-code-preview>