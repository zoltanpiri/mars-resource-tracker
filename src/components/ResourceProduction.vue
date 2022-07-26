<template>
    <div class="production">
        <track-counter/>
    </div>
</template>

<script>
    import TrackCounter from "@/components/TrackCounter";
    export default {
        name: "ResourceProduction",
        components: {TrackCounter}
    }
</script>

<style scoped>
    .production {
        color: #eeeeee;
    }
</style>