<template>
    <div id="trialbox" class="bright">
        <b-container fluid class="test-container">
            <b-row class="rows text-center"> 
                <b-col class="see-packet" sm="12" md="6">
                    <div class="oekotex-wrapper">
                        <img class="oekotex_logo trial_logo" src="../assets/imgs/oekotex_de.png" alt="Oeko-Tex Certificate"/>
                    </div>
                    <div class="trial-slider">
                        <ul class="slides">
                            <li id="t10">
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-10.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 1 und 15 Feuchttüchern" draggable="false">
                            </li>
                            <li id="t20">
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-20.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 2 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                            <li id="t30">
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-30.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 3 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                            <li id="t40" >
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-40.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 4 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                            <li id="t50">
                                <img itemprop="image" src="../assets/imgs/lillydoo-testpaket-50.jpg" alt="Lillydoo Testpaket mit Windeln in Größe 5 und 15 Feuchttüchern" draggable="false"/> 
                            </li>
                        </ul>
                    </div>
                </b-col>
                <b-col class="select-packet" sm="10" md="5" offset-md="1">
                    <h2>Unser gratis Testpaket</h2>
                    <p class="margin-bottom-10 uppercase">Wähle Deine Größe</p>
                    <b-button-group class="text-center margin-bottom-30 button-packet-group" size="lg">
                        <b-button v-on:click="activatePaket(10)" id="b1" class="button-packet"><p>1</p><span>(2-3 KG)</span></b-button>
                        <b-button v-on:click="activatePaket(20)" class="button-packet"><p>2</p><span>(3-4 KG)</span></b-button>
                        <b-button v-on:click="activatePaket(30)" class="button-packet"><p>3</p><span>(4-7 KG)</span></b-button>
                        <b-button v-on:click="activatePaket(40)" class="button-packet"><p>4</p><span>(7-10 KG)</span></b-button>
                        <b-button v-on:click="activatePaket(50)" class="button-packet"><p>5</p><span>(10-12 KG)</span></b-button>
                    </b-button-group>
                    <p>
                        Teste jetzt unsere Windeln und Feuchttücher - In Größe 1 - 3 enthält unser Testpaket 
                        unsere Feuchttücher mit 99 % Wasser, ab Gr. 4 erhältst Du unsere Sensitiven Feuchttücher. 
                        Wir zahlen die Produkte, Du nur den Versand.
                    </p>
                    <ul>
                        <li class="primary-color">
                            Automatischer Übergang ins jederzeit kündbare Windel-Abo für 49,50&nbsp;€ pro Lieferung.
                        </li>
                        <li>
                            Preise inkl. MwSt., ggf. zzgl. <a class="primary-color">Versandkosten</a>
                        </li>
                    </ul>
                    <b-row>
                        <b-col class="text-center" sm="12">
                            <b-button class="trial-button">In den Warenkorb legen</b-button>
                        </b-col>
                    </b-row>
                </b-col>
                
            </b-row>
        </b-container>
    </div>
</template>


<script>
export default {
    data() {
        return {
          wipes: null
        }
    },
    methods: {
        activatePaket(id) {
            let v10 = document.getElementById("t10");
            let v20 = document.getElementById("t20");
            let v30 = document.getElementById("t30");
            let v40 = document.getElementById("t40");
            let v50 = document.getElementById("t50");
            let b1 = document.getElementById("b1");
            
            if(id==20){

                this.wipes = 1;
                this.$emit("testPaket",this.wipes);

                v10.style.opacity = 0;
                v10.style.zIndex = 1;
                v20.style.opacity = 1;
                v20.style.zIndex = 2;
                v30.style.opacity = 0;
                v30.style.zIndex = 1;
                v40.style.opacity = 0;
                v40.style.zIndex = 1;
                v50.style.opacity = 0;
                v50.style.zIndex = 1;
                b1.style.color = "#7c7c7c";
                b1.style.backgroundColor = "transparent";
                b1.style.borderColor = "#7c7c7c";
               
            }
            else if(id==30) {

                this.wipes = 1;
                this.$emit("testPaket",this.wipes);

                v10.style.opacity = 0;
                v10.style.zIndex = 1;
                v20.style.opacity = 0;
                v20.style.zIndex = 1;
                v30.style.opacity = 1;
                v30.style.zIndex = 2;
                v40.style.opacity = 0;
                v40.style.zIndex = 1;
                v50.style.opacity = 0;
                v50.style.zIndex = 1;    
                b1.style.color = "#7c7c7c";
                b1.style.backgroundColor = "transparent";
                b1.style.borderColor = "#7c7c7c";            
            }
            else if(id==40) {

                this.wipes = 2;
                this.$emit("testPaket",this.wipes);

                v10.style.opacity = 0;
                v10.style.zIndex = 1;
                v20.style.opacity = 0;
                v20.style.zIndex = 1;
                v30.style.opacity = 0;
                v30.style.zIndex = 1;
                v40.style.opacity = 1;
                v40.style.zIndex = 2;
                v50.style.opacity = 0;
                v50.style.zIndex = 1;
                b1.style.color = "#7c7c7c";
                b1.style.backgroundColor = "transparent";
                b1.style.borderColor = "#7c7c7c";             
            }
            else if(id==50) {

                this.wipes = 2;
                this.$emit("testPaket",this.wipes);

                v10.style.opacity = 0;
                v10.style.zIndex = 1;
                v20.style.opacity = 0;
                v20.style.zIndex = 1;
                v30.style.opacity = 0;
                v30.style.zIndex = 1;
                v40.style.opacity = 0;
                v40.style.zIndex = 1;
                v50.style.opacity = 1;
                v50.style.zIndex = 2;
                b1.style.color = "#7c7c7c";
                b1.style.backgroundColor = "transparent";
                b1.style.borderColor = "#7c7c7c";
            }
            else {

                this.wipes = 1;
                this.$emit("testPaket",this.wipes);

                v10.style.opacity = 1;
                v10.style.zIndex = 2;
                v20.style.opacity = 0;
                v20.style.zIndex = 1;
                v30.style.opacity = 0;
                v30.style.zIndex = 1;
                v40.style.opacity = 0;
                v40.style.zIndex = 1;
                v50.style.opacity = 0;
                v50.style.zIndex = 1;
                b1.style.color = "#fff";
                b1.style.backgroundColor = "#00AFAB";
                b1.style.borderColor = "#00AFAB";
            }

        }
    }
}
</script>


<style lang="scss" scoped>

$oekotexPosition: relative;

$slidesListStyle: none;

$liWidth: 100%;
$liFloat: left;
$liMarginRight: -100%;
$liMarginLeft: -1%;
$liPosition: relative;
$liOpacity: 1;
$liDisplay: block;
$liZIndex: 2;

$seeMargin: 0;

$opacity10: 1;
$zIndex10: 2;

$selectAlign: left;

$h2FontSize: 1.688rem;
$h2LineHeight: 1.2;
$h2FontWeight: 500;

$ulMarginLeft: 15px;

$liPadding: 0;

$packetPFonTSize: .938rem;

$buttonGroupWidth: 100%;

$buttonHeight: auto;
$buttonWidth: 30%;
$buttonPadding: 7px 5px 2px 5px !important;
$buttonMarginRight: 10px;
$buttonRadius: 0 !important;
$buttonBorder: 1px solid #7c7c7c;
$buttonColor: #7c7c7c;
$buttonBackground: transparent;
$buttonHoverColor: #fff;
$buttonHoverBackground: #00AFAB;
$buttonShadow: none;
$buttonPFontSize: 1.3rem;
$buttonLineHeight: 1;
$buttonPMargin: 0;
$buttonSpanFontSize: .8rem;

$buttonTrialColor: #00AFAB;
$buttonTrialBorderColor: #99dfdd;
$buttonTrialBorder: 0;
$buttonTrialBorderStyle: solid;
$buttonTrialWidth: 100%;
$buttonTrialHeight: 45px;
$buttonTrialTextTransf: uppercase;
$buttonTrialMarginTop: 14px;
$buttonTrialMarginBottom: 10px;
$buttonTrialFontSize: 1.063rem;
$buttonTrialTransition: background-color .3s ease-out;

$trialLogoMarginTop: 8%;
$trialLogoLeft: 14%;
$trialLogoRight: 0%;
$trialLogoZIndex: 10;
$trialLogoWidth: 25%;

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
            margin-left: $liMarginLeft;
            position: $liPosition;
            display: $liDisplay;

        }
    }
}

#t10 {
    opacity: $opacity10;
    z-index: $zIndex10;
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

    p {
        font-size: $packetPFonTSize;
    }

    ul {
        padding-left: $ulMarginLeft;
    }

    li {
        font-size: $packetPFonTSize;
        padding: $liPadding;
    }
}

.button-packet-group {
    width: $buttonGroupWidth;
}

#b1 {
    background-color: $buttonHoverBackground;
    border-color: $buttonHoverBackground;
    box-shadow: $buttonShadow;
    color: $buttonHoverColor;
}

.button-packet {
    padding: $buttonPadding;
    width: $buttonWidth;
    height: $buttonHeight;
    margin-right: $buttonMarginRight;
    border-radius: $buttonRadius;
    border: $buttonBorder;
    color: $buttonColor;
    background-color: $buttonBackground;
    box-shadow: $buttonShadow;

    &:hover {
        background-color: $buttonHoverBackground;
        border-color: $buttonHoverBackground;
        box-shadow: $buttonShadow;
    }

    &:active {
        background-color: $buttonHoverBackground;
        border-color: $buttonHoverBackground;
        box-shadow: $buttonShadow;
        color: $buttonHoverColor;
    }

    &:focus {
        background-color: $buttonHoverBackground;
        border-color: $buttonHoverBackground;
        box-shadow: $buttonShadow;
        color: $buttonHoverColor;
    }

    p {
        font-size: $buttonPFontSize;
        line-height: $buttonLineHeight;
        margin: $buttonPMargin;
    }

    span {
        line-height: $buttonLineHeight;
        font-size: $buttonSpanFontSize;
    }
}

.primary-color {
    color: $buttonHoverBackground !important;
}

.trial-button {
    font-size: $buttonTrialFontSize;
    background-color: $buttonTrialColor;
    border-color: $buttonTrialBorderColor;
    border-radius: $buttonTrialBorder;
    border-width: $buttonTrialBorder;
    border-style: $buttonTrialBorderStyle;
    height: $buttonTrialHeight;
    width: $buttonTrialWidth;
    text-transform: $buttonTrialTextTransf;
    transition: $buttonTrialTransition;

    &:hover {
        background-color: $buttonTrialBorderColor;
    }
}

.trial_logo {
    margin-top: $trialLogoMarginTop;
    left: $trialLogoLeft;
    right: $trialLogoRight;
    z-index: $trialLogoZIndex;
    width: $trialLogoWidth;
}
</style>
