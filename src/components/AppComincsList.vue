<!-- script-section -->
<script>
// import-AppSeriesCards.vue
import AppSeriesCards from './AppSeriesCards.vue';

export default{
    // name-&-components
    name: "AppComicsList",
    components: {
        AppSeriesCards,
    },
    data(){
        return{
            seriesIcons: [
                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                        seriesPrice: "$19.99",
                        nameSeries: "Action Comics",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                        seriesPrice: "$3.99",
                        nameSeries: "American Vampire 1976",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                        seriesPrice: "$16.99",
                        nameSeries: "Aquaman",
                        seriesType: "graphic novel"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                        seriesPrice: "$2.99",
                        nameSeries: "Batgirl",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        seriesPrice: "$3.99",
                        nameSeries: "Batman",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        seriesPrice: "$2.99",
                        nameSeries: "Batman Beyond",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                        seriesPrice: "$3.99",
                        nameSeries: "Batman/Superman",
                        seriesType: "comic book"
                    },
                    
                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                        seriesPrice: "$4.99",
                        nameSeries: "Batman/Superman Annual",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                        seriesPrice: "$5.99",
                        nameSeries: "Batman: The Joker War Zone",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                        seriesPrice: "$6.99",
                        nameSeries: "Batman: Three Jokers",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                        seriesPrice: "$4.99",
                        nameSeries: "Batman: White Knight Presents: Harley Quinn",
                        seriesType: "comic book"
                    },

                    {
                        seriesHref: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                        seriesPrice: "$16.99",
                        nameSeries: "Catwoman",
                        seriesType: "graphic novel"
                    }
                ]
            
        }
    }
}
</script>
<!-- /script-section -->

<!-- template-section -->
<template>

 <section class="comics-series">
        <div class="comics-container">

            <!-- series-cards -->
            <div class="series-cards">
                <AppSeriesCards 
                    v-for="(serie, index) in seriesIcons" 
                    :key="index" 
                    :imgUrl="serie.seriesHref" 
                    :nameSeries="serie.nameSeries" 
                    :seriesPrice="serie.seriesPrice"
                />
            </div>
            <!-- /series-cards -->

            <!-- button -->
            <button class="botton">LOAD MORE</button>
            <!-- /button -->
            
        </div>
    </section>
</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss" scoped>

// mixin-&-variables
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// // comics-series-formatting-section
.comics-series{
    background-color: $secondary;

    // comics-container-formatting-section
    .comics-container{
        color: white;
        flex-direction: column;
        @include flex-center();
        .series-cards{
            display: flex;
            flex-wrap: wrap;
            padding: 1em 0;
        }
        .botton{
            color: white;
            font-size: .9rem;
            text-align: center;
            padding: .3em 3em;
            border: 3px solid white;
            border-radius: 50px;
            background-color: $primary;
            margin-bottom: 3em;
            margin-top: 3em;
            transition-duration: 1s;

            &:hover{
                cursor: pointer;
                color: $primary;
                background-color: white;
                transform: scale(.9);
                border: 3px solid $primary; 
            }
        }
    }
}
</style>
<!-- /style-section -->