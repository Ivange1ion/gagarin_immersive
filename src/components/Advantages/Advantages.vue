<script setup></script>

<template>
    <div id="advantages">
        <div class="part_head">
            Преимущества проекта
        </div>
        <div class="adv_ul">
            <div class="adv_li">
                <div class="adv_li_head">
                    Для рынка развлечений и культуры
                </div>
                <div>
                    Мы предлагаем увеличение прибылей через 
                    возможность оказания дополнительной услуги (нашего VR-экспириенса) 
                </div>
            </div>
            <div class="adv_li">
                <div class="adv_li_head">
                    Для маркетологического рынка
                </div>
                <div>
                    Мы предлагаем психофизиологические исследования и
                    проверки бизнес и технических гипотез относительно продуктов в метаверс.
                </div>
            </div>

            <div class="adv_li">
                <div class="adv_li_head">
                    Для рынка образования
                </div>
                <div>
                    Мы предлагаем воспроизводимый образовательный VR-контент 
                    с высоким потенциалом вовлечения
                </div>
            </div>
            <div class="adv_li">
                <!-- <img src="../../assets/img/pl 2.webp" alt=""> -->
                <div class="adv_li_head">
                    Для рынка корпоративного и государственного управления
                </div>
                <div>
                    Мы предлагаем персонализированные иммерсивные 
                    VR-инструменты  психологической диагностики с высокой степенью погружения
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    #advantages{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .adv_ul{
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 60px 100px; 
    }
    .adv_li{
        margin-bottom: 10px;
        border-left: #FF8D28 solid 4px;
        padding-left: 10px;
    }
    .adv_li_head{
        font-weight: bold;
        font-size: 30px;
        padding-bottom: 10px;
    }
    @media (width<730px) {
            .adv_ul{
                display: grid;
                grid-template-columns: 1fr;
                gap:20px;
            }
    }
    img{
        width: 75px;
        height: 75px;
    }
</style>
