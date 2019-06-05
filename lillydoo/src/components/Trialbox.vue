<template>
    <div id="trialbox" class="bright">
        <b-container fluid class="test-container">
            <b-row class="rows text-center"> 
                <b-col class="see-packet" sm="10" md="5">
                    <div class="oekotex-wrapper">
                        <img class="oekotex_logo" src="../assets/imgs/oekotex_de.png" alt="Oeko-Tex Certificate"/>
                    </div>
                    <div class="trial-slider">
                        <ul class="slides">
                            <li>
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-10.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 1 und 15 Feuchttüchern" draggable="false">
                            </li>
                            <li>
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-20.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 2 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                            <li>
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-30.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 3 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                            <li>
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-40.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 4 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                            <li>
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-50.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 5 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                        </ul>
                    </div>
                </b-col>
                <b-col class="select-packet" sm="10" md="5" offset-md="2">
                    <h2>Unser gratis Testpaket</h2>
                    <p class="margin-bottom-10 uppercase">Wähle Deine Größe</p>
                    <b-button-group class="margin-bottom-30">
                        <b-button>Button 1</b-button>
                        <b-button>Button 2</b-button>
                        <b-button>Button 3</b-button>
                        <b-button>Button 3</b-button>
                        <b-button>Button 3</b-button>
                    </b-button-group>
                    <p>
                        Teste jetzt unsere Windeln und Feuchttücher - In Größe 1 - 3 enthält unser Testpaket 
                        unsere Feuchttücher mit 99 % Wasser, ab Gr. 4 erhältst Du unsere Sensitiven Feuchttücher. 
                        Wir zahlen die Produkte, Du nur den Versand
                    </p>
                    <ul>
                        <li></li>
                        <li></li>
                    </ul>
                    <b-row>
                        <b-col sm="12">
                            <b-button>In den Warenkorb legen</b-button>
                        </b-col>
                    </b-row>
                </b-col>
                
            </b-row>
        </b-container>
    </div>
</template>

<style lang="scss" scoped>

$oekotexPosition: relative;

$slidesListStyle: none;

$liWidth: 100%;
$liFloat: left;
$liMarginRight: -100%;
$liPosition: relative;
$liOpacity: 1;
$liDisplay: block;
$liZIndex: 2;

$seeMargin: 0;

$selectAlign: left;

$h2FontSize: 1.688rem;
$h2LineHeight: 1.2;
$h2FontWeight: 500;

.oekotex-wrapper {
    position: $oekotexPosition;
}

.trial-slider {
    
    .slides {
        list-style: $slidesListStyle;

        li {
            width: $liWidth;
            float: $liFloat;
            margin-right: $liMarginRight;
            position: $liPosition;
            opacity: $liOpacity;
            display: $liDisplay;
            z-index: $liZIndex;
        }
    }
}

.see-packet {
    margin: $seeMargin;
}

.select-packet {

    text-align: $selectAlign;
    
    h2 {
        font-size: $h2FontSize;
        line-height: $h2LineHeight;
        font-weight: $h2FontWeight;
    }
}



</style>
