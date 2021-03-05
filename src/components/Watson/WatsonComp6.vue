<template>
    <div>{{text}}</div>
</template>

<script>
export default {
    data() {
        return{
            text: ".",
            currentFrame: 0,
            frames: ["Loading..........",".Loading.........","..Loading........","...Loading.......","....Loading......",".....Loading.....","......Loading....",".......Loading...","........Loading..",".........Loading.", "..........Loading"]
        }
    },
    created() {
    this.interval = setInterval(() => this.loading(), 100);
    },
    methods:
    {
        loading()
        {
            this.text = this.frames[this.currentFrame];
            this.currentFrame++;
            if (this.currentFrame >= this.frames.length)
            {
                this.currentFrame = 0;
            }
        }
    }
}
</script>

<style scoped>
    div {
        display: inline;
    }
</style>