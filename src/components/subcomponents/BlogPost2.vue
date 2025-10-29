<script>
export default {
    name: 'BlogPost',
    props: {
        subject: String,
        entry: String,
        mood: String,
    },
    computed: {
        imgLoc() {
            return `/assets/${this.mood.toLowerCase()}.png`;
        }
    }
}
</script>

<template>
    <div class="card" style="width: 18rem;">
        <img :src="imgLoc" class="card-img-top" alt="Mood image" />
        <div class="card-body">
            <h5 class="card-title">{{ subject }}</h5>
            <p class="card-text">{{ entry }}</p>
            <slot></slot>
        </div>
    </div>
</template>
