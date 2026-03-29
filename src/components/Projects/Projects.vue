<script setup>
    import Button from "../UI/Button.vue";
</script>

<template>
    <div id="projects">
        <div class="part_head">
            Другие проекты
        </div>
        <div class="text-item">
            У нашей компании имеется успешный опыт в разработке коммерческих продуктов виртуальной реальности!
        </div>
        <div id="projects-cards">
            <div class="card">
                <img class="project-img" src="../../assets/img/blood.webp" alt="">
                <div class="card-text">
                    <div>
                        <div class="card-head text-item">Сердечно-соссудистая система</div>
                        <hr>
                        <div class="card-info text-item">Станьте клеткой внутри организма, исследуйте его изнутри</div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
            <div class="card">
                <img class="project-img" src="../../assets/img/insects.webp" alt="">
                <div class="card-text">
                    <div>
                        <div class="card-head text-item">Мир насекомых</div>
                        <hr>
                        <div class="card-info text-item">Станьте клеткой внутри организма, исследуйте его изнутри</div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
            <div class="card">
                <img class="project-img" src="../../assets/img/newyear.webp" alt="">
                <div class="card-text">
                    <div>
                        <div class="card-head text-item">Новогоднее путешествие</div>
                        <hr>
                        <div class="card-info text-item">Станьте клеткой внутри организма, исследуйте его изнутри</div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
            <div class="card">
                <img class="project-img" src="../../assets/img/sun.webp" alt="">
                <div class="card-text">
                    <div>
                        <div class="card-head text-item">Солнечная система</div>
                        <hr>
                        <div class="card-info text-item">Станьте клеткой внутри организма, исследуйте его изнутри</div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .detail{
        font-size: 25px;
        font-weight: bold;
        width: 70%;
        background-color: #ff8d28;
        color: black;
        border-radius: 60px;
        text-align: center;
        padding: 15px;
        position: relative;
        left: 15%;
        bottom: 0;
    }
    .card-info{
        font-size: 30px;
    }
    .project-img{
        max-width: 200px;
        height: 300px;
    }
    .card{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        margin-top: 30px;
    }
    .card-head{
        color: var(--text-span);
    }
    .card-text{
        width: 60%;
        display: flex;
        justify-content: space-between;
        flex-direction: column;
    }
    @media (width<550px) {
        .card-text{
            width: 100%;
        }
        .card-info{
            font-size: 20px;
        }
        .detail{
            width: 100%;
            left: auto;
        }
    }
    @media (min-width:1000px) {
        .card{
            justify-content: space-around;
        }
    }
</style>
