<template>
    <div id="content" class="bright">
        <b-container fluid class="content-container">
            <b-row class="rows text-center">
                <b-col sm="12">
                    <h2 class="margin-bottom-20">Dein Testpaket enthält</h2>
                </b-col>
            </b-row>
            <b-row class="rows text-center">
                <b-col class="margin-bottom-20" sm="12" md="6">
                    <b-row class="rows text-center">
                        <b-col class="trial-contains-img" sm="3">
                            <img src="../assets/imgs/lillydoo-little-blowballs-design-preview-tp.jpg" alt="Lillydoo Windel Design - Little Blowballs"/>
                        </b-col>
                        <b-col class="trial-info" sm="8">
                            <h4 class="uppercase margin-bottom-10">10 Lillydoo Windeln</h4>
                            <ul>
                                <li>0 % Parfüme &amp; Lotionen, 100 % LILLYDOO Schutz</li>
                                <li>Extra weich und mit idealer Passform</li>
                            </ul>
                        </b-col>
                    </b-row>
                </b-col>
                <b-col class="margin-bottom-20" sm="12" md="6">
                    <b-row class="rows text-center">
                        <b-col class="trial-contains-img" sm="3">
                            <img v-if="this.wipes!=2" src="../assets/imgs/water-wipes-15-small.jpg" alt="LILLYDOO 15 Feuchttücher mit 99% Wasser"/>
                            <img v-if="this.wipes==2" src="../assets/imgs/sensitive-wipes-15-small.jpg" alt="LILLYDOO 15 sensitive Feuchttücher"/>
                        </b-col>
                        <b-col  v-if="this.wipes!=2" class="trial-info" sm="8">
                            <h4>15 Feuchttücher mit 99 % Wasser</h4>
                            <ul>
                                <li>0 % Parfüme &amp; PEGs, 100 % biologisch abbaubar</li>
                                <li>Extra dickes und kompostierbares Tuch</li>
                            </ul>
                        </b-col>
                        <b-col v-if="this.wipes==2" class="trial-info" sm="8">
                            <h4>15 sensitive Feuchttücher</h4>
                            <ul>
                                <li>0 % Parfüme &amp; PEGs, 100 % biologisch abbaubar</li>
                                <li>Extra dickes und kompostierbares Tuch</li>
                            </ul>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
export default {
    props: ['wipes']
}
</script>


<style lang="scss" scoped>

$rowsScreenPaddingTop: .6rem;
$rowsScreenPaddingBottom: .4rem;

$trialScreenPadding: .938rem;

$trialImgScreenWidth: 30%;
$trialImgScreenPadding: 0 !important;

$trialInfoScreenWidth: 63%;

$h2FontSize: 1.688rem;
$h2LineHeight: 1.2;
$h2FontWeight: 500;

$trialImgFloat: left;
$trialImgMarginRight: 20px;

$trialInfoAlign: left;
$trialInfoPadding: 0;

$h4FontSize: 1.063rem;
$h4FontFamily: CeraProMedium,Helvetica,Roboto,Arial,sans-serif;
$h4LineHeight: 1.5;

$ulMarginTop: 0;
$ulMarginBottom: 1rem;
$ulMarginLeft: 1rem;
$ulPaddingLeft: 0;
$ulLineHeight: 1.4;
$ulFontSize: .938rem;

.content-container {

    h2 {
        font-size: $h2FontSize;
        line-height: $h2LineHeight;
        font-weight: $h2FontWeight;
    }
}

@media only screen and (max-width: 52em) {
    .rows {
        padding-top: $rowsScreenPaddingTop;
        padding-bottom: $rowsScreenPaddingBottom;
    }
}

@media only screen and (max-width: 52em) {
    .trial {
        padding-top: $rowsScreenPaddingTop;
        padding-bottom: $rowsScreenPaddingBottom;
    }
}

@media only screen and (max-width: 834px) {
    .trial {
        padding-left: $trialScreenPadding;
        padding-right: $trialScreenPadding;
    }
}


@media only screen and (max-width: 834px) {
    .trial-contains-img {
        width: $trialImgScreenWidth;
        padding: $trialImgScreenPadding;        
    }
}

@media only screen and (max-width: 834px) {
    .trial-info {
        width: $trialInfoScreenWidth;
    }
}

.trial-contains-img {
    float: $trialImgFloat;
    margin-right: $trialImgMarginRight;
}

.trial-info {
    text-align: $trialInfoAlign;
    padding: $trialInfoPadding;
    
    h4 {
        font-size: $h4FontSize;
        font-family: $h4FontFamily;
        line-height: $h4LineHeight;
    }

    ul {
        margin-top: $ulMarginTop;
        margin-bottom: $ulMarginBottom;
        margin-left: $ulMarginLeft;
        padding-left: $ulPaddingLeft;
        line-height: $ulLineHeight;
        font-size: $ulFontSize;
    }
}
</style>
