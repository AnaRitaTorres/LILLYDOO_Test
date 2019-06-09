<template>
    <div id="faqs" class="dark">
        <b-container fluid class="faqs-container">
            <b-row class="rows text-center">
                <b-col sm="12">
                    <h2>Wie es funktioniert</h2>
                </b-col>
            </b-row>
            <b-row class="rows text-center">
                <b-col sm="12" md="12" class="text-center">
                    <ul class="trial-steps">
                        <li class="text-center step">
                            <img src="../assets/imgs/lillydoo-your-trialbox-icon.svg"/>
                            <h4 class="uppercase">Dein Testpaket</h4>
                            <p>Wir schenken Dir die Produkte,<br>Du übernimmst nur das Porto.</p>
                        </li>
                        <li class="text-center step">
                            <img src="../assets/imgs/lillydoo-your-flexibility-icon.svg"/>
                            <h4 class="uppercase">Deine Flexibilität</h4>
                            <p class="margin-bottom-30">Erste Monatsbox nach 14 Tagen für 49,50&nbsp;€ erhalten. Oder noch vor der ersten Lieferung kündigen.</p>
                            <p class="fake-link">Erfahre hier mehr über das <br>LILLYDOO Windel-Abo.</p>
                        </li>
                        <li class="text-center step">
                            <img src="../assets/imgs/lillydoo-your-subscription-icon.svg"/>
                            <h4 class="uppercase">Deine Monatsbox</h4>
                            <p>Jederzeit Designs oder Lieferintervalle anpassen oder die Windelgröße ändern.</p>
                        </li>
                    </ul>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<style lang="scss" scoped>

$h2FontSize: 1.688rem;
$h2LineHeight: 1.2;
$h2MarginBottom: 10px;
$h2FontWeight: 500;

$trialStyle: none;
$trialMargin: 0;

$stepWidth: 33.33333333%;
$stepFloat: left;
$stepPadding: 1.5rem;

$imgWidth: 70px;
$imgMarginBottom:15px;
$imgVerticalAlign: middle;

$h4FontSize: 1.063rem;
$h4FontFamily: CeraProMedium,Helvetica,Roboto,Arial,sans-serif;
$h4LineHeight: 1.5;
$h4MarginBottom: 10px;

$pFontSize: .938rem;
$pMarginBottom: 15px;

$fakeColor: #00afab;

.faqs-container {
    h2 {
        font-size: $h2FontSize;
        line-height: $h2LineHeight;
        margin-bottom: $h2MarginBottom;
        font-weight: $h2FontWeight;
    }
}

@media only screen and (max-width: 834px) {

    .trial-steps .step {
        width: 100% !important;
        float: none !important;
        margin-bottom: 3.75rem;
        padding-left:0 !important;
    }
}

.trial-steps {
    list-style: $trialStyle;
    margin: $trialMargin;

    .step {
        width: $stepWidth;
        float: $stepFloat;
        padding-left: $stepPadding;
        padding-right: $stepPadding;

        img {
            width: $imgWidth;
            margin-bottom: $imgMarginBottom;
            vertical-align: $imgVerticalAlign;
        }

        h4 {
            font-family: $h4FontFamily;
            font-size: $h4FontSize;
            line-height: $h4LineHeight;
            margin-bottom: $h4MarginBottom;
        }

        p {
            font-size: $pFontSize;
            margin-bottom: $pMarginBottom;
        }
    }

    .fake-link {
        color: $fakeColor;
    }
    
    



}
</style>
