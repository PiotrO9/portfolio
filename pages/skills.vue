<script setup lang="ts">

</script>

<template>
    <h1>Skills & Carrier</h1>
    <div class="skills-and-career-wrapper">
        <div class="skills">
            <div class="skill-wrapper">
                <img src="../public/images/css.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/css.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/css.png" alt="" clas>
            </div>
        </div>
        <div class="career">
            <div class="time-line-element">

            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.skills-and-career-wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 1600px;

    .skills {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));

        .skill-wrapper {
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #D0BFBD;
            height: 150px;
            width: 150px;
            border-radius: 50%;

            img {
                height: 80px;
                width: 80px;
            }
        }
    }

    .career {}
}
</style>