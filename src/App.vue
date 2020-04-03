<template>
    <div>
        <form-helper>
            <div slot="form-header">
                <h3>This is the title of a form</h3>
                <h1> hello this is h1 tag</h1>
                <p>This is some info about the form</p>
            </div>
            <div slot="form-fields">
                <input type="text" placeholder="name" required />
                <input type="password" placeholder="password" required />
                
            </div>
            <div slot="form-controls">
                <button v-on:click="handleSubmit">Submit</button>
            </div>

            <div slot="form-etc">
               <input type="text" placeholder="etc" required />
              
            </div>


        </form-helper>
    </div>
</template>

<script>
// Imports
import formHelper from './components/formHelper.vue'
export default {
    components: {
        'form-helper': formHelper
    },
    data () {
        return {
          title:"hello this  Main slot title"
        }
    },
    methods: {
        handleSubmit: function(){
            alert('thanks for submitting');
        }
    }
}
</script>

<style>
body{
    margin: 0;
    font-family: 'Nunito SemiBold';
}
</style>
