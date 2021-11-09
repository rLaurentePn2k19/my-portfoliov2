<template>
    <div class="btn-group-bottom-right-fixed d-flex flex-column">
        <div v-for="(btn, i) in formActions" :key="i">
            <v-tooltip left>
                <template v-slot:activator="{ on, attrs }">
                    <v-slide-x-reverse-transition>
                        <v-btn
                            v-scroll="onScroll"
                            v-show="fab"
                            v-bind="attrs"
                            :key="i"
                            v-on="on"
                            dark
                            depressed
                            fab
                            @click="btnAction(btn.name)"
                            class="mb-2"
                            :color="btn.color"
                        >
                            <v-icon> {{ btn.icon }} </v-icon>
                        </v-btn>
                    </v-slide-x-reverse-transition>
                </template>
                <span>{{ btn.name }}</span>
            </v-tooltip>
        </div>
    </div>
</template>

<script>
export default {
    name: 'floatingButton',
    props: {
        formActions: Array
    },
    data() {
        return {
            fab: false
        }
    },
    methods: {
        onScroll(e) {
            if (typeof window === 'undefined') return
            const top = window.pageYOffset || e.target.scrollTop || 0
            this.fab = top > 400
        },
        btnAction(action) {
            if (action === 'Go Up') {
                this.toTop()
            }
        },
        toTop() {
            this.$vuetify.goTo(0, {
                duration: 700,
                offset: 0,
                easing: 'easeInOutCubic'
            })
        }
    }
}
</script>

<style scoped>
.btn-group-bottom-right-fixed {
    position: fixed;
    bottom: 20px;
    right: 20px;
    z-index: 100;
}
</style>