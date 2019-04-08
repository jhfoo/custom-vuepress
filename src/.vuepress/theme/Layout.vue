<template>
    <v-app>
        <v-content>
            <component class="main-content" :is="layout"/>
        </v-content>
    </v-app>
</template>
<script>
import Default from './layouts/Default.vue'
import Home from './layouts/Home.vue'

export default {
    components: {
        Home, Default
    },
    computed: {
        layout() {
            console.log(this.$page.frontmatter.layout)
            if (this.$page.frontmatter.layout) {
                return this.$page.frontmatter.layout
            } else {
                return 'default'
            }
        }
    }
}
</script>