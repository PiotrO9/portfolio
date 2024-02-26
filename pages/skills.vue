

<template>
    <h1 class="heading">Skills & Carrier</h1>
    <div class="skills-and-career-wrapper">
        <div class="skills">
            <div class="skill-wrapper">
                <img src="../public/images/css.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/git.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/html.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/js.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/nuxt.svg" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/ts.png" alt="" clas>
            </div>
            <div class="skill-wrapper">
                <img src="../public/images/vue.png" alt="" clas>
            </div>
        </div>
        <div class="career">
            <TimeLineElement date="01.10" message="Rozpoczęcie studiów na kierunku Informatyka na uczelni WSIZ zaocznie"
                image-name="wsiz.png" />
            <TimeLineElement date="20.06" message="Rozpoczęcie pracy w IDEO Software" image-name="ideo.png" />
        </div>
    </div>
</template>

<style scoped lang="scss">
.heading {
    color: white;
    font-size: 50px;
    text-align: center;
    padding: 30px 0px;

    @media (width > 540px) {
        font-size: 60px;
    }

    @media (width > 768px) {
        font-size: 100px;
        padding: 40px 0px 60px;
    }
}

.skills-and-career-wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: center;

    @media (width > 1024px) {
        flex-direction: row;
    }

    .skills {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 30px;

        @media (width > 400px) {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            align-items: center;
            justify-items: center;
        }

        @media (width > 540px) {
            grid-template-columns: repeat(3, minmax(0, 1fr));
        }

        @media (width > 768px) {
            grid-template-columns: repeat(4, minmax(0, 1fr));
        }

        @media (width > 1024px) {
            width: 50%;
            max-width: 680px;
            grid-template-columns: repeat(3, minmax(0, 1fr));
        }

        @media (width > 1400px) {
            grid-template-columns: repeat(4, minmax(0, 1fr));
        }

        .skill-wrapper {
            display: flex;
            justify-content: center;
            align-items: center;
            // background-color: rgba(208, 191, 189, 0.7);
            // background-color: rgba(207, 202, 172, 0.7);
            background-color: rgba(239, 233, 250, 0.55);
            height: 130px;
            width: 130px;
            border-radius: 30%;

            img {
                height: 50%;
                width: 50%;
                object-fit: cover;
            }
        }
    }

    .career {
        width: 100%;
        display: flex;
        flex-direction: column;

        @media (width > 1024px) {
            width: 50%;
            max-width: 680px;
        }
    }
}
</style>