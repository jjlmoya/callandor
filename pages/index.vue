<template>
    <div>
        <Layout>
            <Typing
                to-type=" La Rueda del tiempo gira y las eras llegan y pasan y dejan tras de sí recuerdos que se convierten en
        leyenda. La leyenda se difumina, deviene mito, e incluso el mito se ha olvidado mucho antes de que la era que lo
        vio nacer retorne de nuevo. En una era llamada la tercera por algunos, una era que ha de venir, una era
        transcurrida hace mucho, comenzó a soplar un viento. El viento no fue el principio, pues no existen comienzos ni
        finales en el eterno girar de la Rueda del Tiempo. Pero aquél fue un principio."
            />
        </Layout>
    </div>
</template>

<style lang="scss">
  @import 'apps.scss';
</style>

<script>
    import SeoService from '../services/seoService'
    import Layout from '@/layouts/Default.vue'
    import Typing from '@/components/Typing/Typing.vue'
    const SEO_PAGE_DATA = new SeoService({
        title: 'Inicio',
        description: 'Home Description'
    })

    export default {
        name: 'Home',
        components: {
            Layout,
            Typing
        },
        head () {
            return SEO_PAGE_DATA.getMetas()
        }
    }
</script>
