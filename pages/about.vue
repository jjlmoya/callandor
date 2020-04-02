<template>
    <div class="about">
        <Layout>
            About
        </Layout>
    </div>
</template>

<script>
    import Layout from '@/layouts/Default.vue'
    export default {
        name: 'DefaultLayout',
        title () {
            return `Foo Page — ${this.someValue}`
        },
        components: {
            Layout
        },
        data () {
            return {
                someValue: 'bar'
            }
        }
    }

</script>
