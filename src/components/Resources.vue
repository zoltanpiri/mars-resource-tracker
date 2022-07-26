<template>
    <div class="container">
        <div class="row">
            <resource-tracker type="credit"/>
            <resource-tracker type="steel"/>
            <resource-tracker type="titanium"/>
            <resource-tracker type="plant"/>
            <resource-tracker type="electricity"/>
            <resource-tracker type="heat"/>
        </div>
    </div>

</template>

<script>
    import ResourceTracker from "@/components/ResourceTracker";
    export default {
        name: "ResourcesComponent",
        components: {ResourceTracker}
    }
</script>

<style scoped>

    .row {
        display: flex;
        flex-direction: row;
        row-gap: 10px;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    .container{
        max-width: 800px;
        margin: 10px auto;
    }

</style>