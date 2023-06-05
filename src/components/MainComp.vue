<script>
import { store } from './../store';
import CardComp from './CardComp.vue'

export default {
    name: 'MainComp',
    components: {
        CardComp
    },
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <main class="bkcolororange">
        <section class="container">
            <div class="bkcolorwhite">
                <div class="row">
                    <div v-for="element in store.playCardList" class="col-6 col-md-4 col-lg-3 mb-5">
                        <CardComp :details="element" />
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style scoped>
.bkcolororange {
    background-color: rgb(212, 143, 56);
    padding: 30px;
}

.bkcolorwhite {
    background-color: white;
    padding: 30px;
}
</style>
