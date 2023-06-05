<script>
export default {
    name: 'CardComp',
    props: {
        details: Object
    }
}
</script>

<template>
    <section class="character text-center">
        <div class="bkcolororange">
            <img class="img-fluid mb-3" :src="details.card_images[0].image_url">
            <div class="text-height">
                <h4>{{ details.name }}</h4>
                <div>{{ details.type }}</div>
            </div>
        </div>
    </section>
</template>
  
<style scoped>
.bkcolororange {
    background-color: rgb(212, 143, 56);
}

.text-height {
    height: 100px;
}
</style>
  