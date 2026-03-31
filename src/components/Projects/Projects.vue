<script setup>
    import Button from "../UI/Button.vue";
</script>

<template>
    <div id="projects">
        <div class="part_head">
            Другие проекты
        </div>
        <div class="text-item center-aling">
            У нашей компании имеется успешный опыт в разработке коммерческих продуктов виртуальной реальности!
        </div>
        <div id="projects-cards">
            <div class="card">
                <img class="project-img" src="../../assets/img/blood.webp" alt="">
                <div class="card-text center-aling">
                    <div>
                        <div class="card-head text-item">Сердечно-соссудистая система</div>
                        <hr>
                        <div class="card-info text-item">Вы познакомитесь с нашими неутомимыми помощниками – клетками крови. 
                            Вместе с эритроцитами доставите к тканям ценный кислород. 
                            Нейтрализуете вредоносные бактерии с лейкоцитами. 
                            С командой тромбоцитов окажете первую помощь при кровотечении. 
                            А ещё узнаете, как помочь своей сердечно-сосудистой системе работать исправно!
                        </div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
            <div class="card">
                <img class="project-img" src="../../assets/img/insects.webp" alt="">
                <div class="card-text center-aling">
                    <div>
                        <div class="card-head text-item">Мир насекомых</div>
                        <hr>
                        <div class="card-info text-item">Насекомые – самые таинственные существа на нашей планете. 
                            Некоторые из них существовали ещё до динозавров. Сегодня на Земле могут жить до 5 миллионов видов насекомых, 
                            науке же известен лишь миллион из них. Приглашаем вас узнать секреты этих маленьких супергероев!
                        </div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
            <div class="card">
                <img class="project-img" src="../../assets/img/newyear.webp" alt="">
                <div class="card-text center-aling">
                    <div>
                        <div class="card-head text-item">Новогоднее путешествие</div>
                        <hr>
                        <div class="card-info text-item">Вы побываете в разных уголках нашей страны и узнаете, 
                            где раньше всех в России начинают встречать Новый год, откуда взялись традиции 
                            наряжать ёлочку и дарить подарки, как зовут других российских Дедушек 
                            и где находится терем Снегурочки. Вы полюбуетесь полярным сиянием и полетаете в волшебных санях. 
                            Вас ждут невероятные встречи и весёлые загадки!
                        </div>
                    </div>
                    <!-- <Button class="detail">Подробнее</Button> -->
                     <button class="detail">Подробнее</button>
                </div>
            </div>
            <div class="card">
                <img class="project-img" src="../../assets/img/sun.webp" alt="">
                <div class="card-text center-aling">
                    <div>
                        <div class="card-head text-item">Солнечная система</div>
                        <hr>
                        <div class="card-info text-item">Готовы к познавательным приключениям?!
                            Летим к удивительным мирам, которые
                            вращаются вокруг яркого Солнца. В этом VR-фильме вы окажетесь в самом
                            сердце космоса, посетите разные планеты, узнаете про спутники и уникальныеявления.
                        </div>
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
        max-width: 60%;
    }
    .card-info{
        font-size: 30px;
    }
    .project-img{
        max-width: 300px;
        height: 400px;
    }
    .card{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        margin-top: 30px;
    }
    .card-text div{
        margin-bottom: 10px;
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
    @media (width<803px) {
        .card{
            justify-content: center;
            margin-bottom: 50px;
        }
        .card-text{
            width: 100%;
            text-align: center;
            align-items: center;
        }
        .card-info{
            font-size: 20px;
        }
        .detail{
            width: 100%;
            left: auto;
        }
        .project-img{
            max-width: 200px;
            height: 300px;
        }
    }
    @media (min-width:1000px) {
        .card{
            justify-content: space-around;
        }
    }
</style>
