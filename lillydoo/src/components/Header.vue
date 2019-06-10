<template>
    <div id="header">
        <b-container fluid class="header-container text-center">
            <img class="oekotex_logo" src="../assets/imgs/oekotex_de.png" alt="Oeko-Tex Certificate"/>
            <b-row class="rows text-center">
                <b-col sm="12" md="6">
                    <h1 class="margin-bottom-10">Entdecke unsere Hautfreundlichkeit</h1>
                    <b-button class="header-button">Jetzt Deine Größe wählen</b-button>
                </b-col>
            </b-row>
        </b-container>      
    </div>
</template>

<style lang="scss" scoped>
@import '../scss/fonts.scss';

$containerPosition: relative;
$containerBackground: url('../assets/imgs/lillydoo-testpaket-header-large.jpg');
$containerBackgroundSize: cover;
$containerBackgroundPosition: center;
$containerBackgroundRepeat: no-repeat;
$containerBackgroundColor:  #f8f8f8;
$containerDisplay: flex;
$containerPadding: 0;
$containerMargin: 0;
$containerWidth: 100%;
$containerHeight: auto;
$containerAlignSelf: flex-end;


$h1FontFamily: Museo300,Helvetica,Roboto,Arial,sans-serif;
$h1FontSize: 2.625rem;
$h1LineHeight: 1.1;
$h1PaddingTop: 20%;

$h1ScreenFontSize: 2.188rem;

$rowHeight: 50%;

$buttonColor: #00AFAB;
$buttonBorderColor: #99dfdd;
$buttonBorder: 0;
$buttonBorderStyle: solid;
$buttonHeight: 45px;
$buttonTextTransf: uppercase;
$buttonMarginTop: 14px;
$buttonMarginBottom: 10px;
$buttonFontSize: 1.063rem;
$buttonTransition: background-color .3s ease-out;

.header-container {
    position: $containerPosition;
    background: $containerBackground;
    background-size: $containerBackgroundSize;
    background-position: $containerBackgroundPosition;
    background-repeat: $containerBackgroundRepeat;
    background-color: $containerBackgroundColor;
    display: $containerDisplay;
    padding-top: $containerPadding;
    padding-bottom: $containerPadding;
    margin-right: $containerMargin;
    margin-left: $containerMargin;
    width: $containerWidth;
    height: $containerHeight;
    min-width: $containerWidth;
    align-self: $containerAlignSelf;
}

.header-container {
    h1 {
        font-family: $h1FontFamily;
        font-size: $h1FontSize;
        line-height: $h1LineHeight;
        padding-top: $h1PaddingTop;
    }
}

@media only screen and (max-width: 834px) {

    .header-container {
        h1 {
            font-size: $h1ScreenFontSize;
        }
    }
}

.header-button {
    font-size: $buttonFontSize;
    background-color: $buttonColor;
    border-color: $buttonBorderColor;
    border-radius: $buttonBorder;
    border-width: $buttonBorder;
    border-style: $buttonBorderStyle;
    height: $buttonHeight;
    text-transform: $buttonTextTransf;
    transition: $buttonTransition;

    &:hover {
        background-color: $buttonBorderColor;
    }
}

</style>

