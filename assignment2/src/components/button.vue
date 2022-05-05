<template>
    <div class="button">
        <p @click="happened" class="btn-text">{{ isReverse }} {{ staySameText }}</p>
    </div>
</template>

<script>
export default {
    props: ['isReverse', "staySameText"],
    name: "BaseButton",
    data() {
        return {
            title: "Primary",
        }
    },
    methods: {
        happened () {
            this.$emit('isClicked', this.isReverse);
            console.log(this.title, "Click Happened");
        },
    }
}
</script>

<style scoped>
    .button{
        display: flex;
        flex-direction: column;
        align-content: center;
        justify-content: center;
        text-align: center;
        box-sizing: border-box;
        width: 300px;
        height: 100px;
        background-color: rgba(126, 214, 223, 0.6);
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 20px;
        border-radius: 10px;
    }

    .btn-text{
        font-family: sans-serif;
        font-size: 2em;
        color: #ffffff;
        font-weight: 400;
    }


</style>