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
                            <img class="wipes1" src="../assets/imgs/water-wipes-15-small.jpg" alt="LILLYDOO 15 Feuchttücher mit 99% Wasser"/>
                            <img class="wipes2" src="../assets/imgs/sensitive-wipes-15-small.jpg" alt="LILLYDOO 15 sensitive Feuchttücher"/>
                        </b-col>
                        <b-col class="trial-info wipes1" sm="8">
                            <h4>15 Feuchttücher mit 99 % Wasser</h4>
                            <ul>
                                <li>0 % Parfüme &amp; PEGs, 100 % biologisch abbaubar</li>
                                <li>Extra dickes und kompostierbares Tuch</li>
                            </ul>
                        </b-col>
                        <b-col class="trial-info wipes2" sm="8">
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
    props: ['wipes'],
    data() {
        return {
            wipesVar: this.wipes
        }
    },
    mounted() {
        this.$nextTick(() => {
            let w1_img = document.getElementsByClassName('wipes1')[0];
            let w1_text = document.getElementsByClassName('wipes1')[1];
            let w2_img = document.getElementsByClassName('wipes2')[0];
            let w2_text = document.getElementsByClassName('wipes2')[1];
           
            if(this.wipesVar==1) {
                w1_img.style.display = "block"; 
                w1_text.style.display = "block"; 
                w2_img.style.display = "none";
                w2_text.style.display = "none";
            }
            else {
                w1_img.style.display = "none";
                w1_text.style.display = "none";
                w2_img.style.display = "block"; 
                w2_text.style.display = "block"; 
            }
        })
    }
}
</script>


<style lang="scss" scoped>

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
.trial-contains-img {
    float: $trialImgFloat;
    margin-right: $trialImgMarginRight;
}

.trial-info {
    float: left;
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

.wipes1 {
    display: block;
}

.wipes2 {
    display: none;
}

</style>
