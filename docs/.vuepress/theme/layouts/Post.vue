<template>
    <v-app light>
        <v-container>
            <v-layout row wrap align-center>
                <v-flex xs12>
                    <header >
                        Published on the {{ date }}
                    </header>
                </v-flex>

                <article>
                    <Content :custom="false"/>
                </article>
            </v-layout>
        </v-container>
    </v-app>
</template>

<script>
import moment from 'moment'

export default {
    computed:{
        date(){
            return moment(String(this.$page.frontmatter.date)).format('MM/DD/YYYY')
        }
    }
}
</script>
