<template>
     <div class="item">
        <div class="row">
            <div class="column">
                <img :src="iconSrc" :alt="type"/>
            </div>
            <div class="column">
                <resource-value/>
                <resource-production/>
            </div>
         </div>
    </div>
</template>

<script>
    import ResourceValue from "@/components/ResourceValue";
    import ResourceProduction from "@/components/ResourceProduction";
    export default {
        name: "ResourceTracker",
        components: {ResourceProduction, ResourceValue},
        props: {
            type: String
        },
        computed: {
            iconSrc() {
                return '../assets/icons/'+this.type+'.png';
            }
        }
    }
</script>

<style scoped>
    .item{
        width: 210px;
        height:100px;
        background: rgb(59,41,22);
        background: linear-gradient(0deg, rgba(59,41,22,1) 50%, rgba(255,255,255,1) 50%);
        display: inline-block;
        border: 2px solid #eeeeee;
        border-radius: 17px;
        margin: 10px 10px 10px 40px;
        box-shadow: #666666 3px 3px 8px;
    }
    img {
        width: 60px;
        height: 60px;
        margin-left: -35px;
        border: 2px solid #eeeeee;
        border-radius: 17px;
    }
    .column{
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        height: 100px;
    }
    .row{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
    }

</style>