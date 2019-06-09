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

$containerBackground: url('../assets/imgs/lillydoo-testpaket-header-large.jpg');
$containerWidth: 100%;
$containerHeight: 36vw;
$containerMaxHeight: 550px;
$containerDisplay: flex;

$h1FontFamily: Museo300,Helvetica,Roboto,Arial,sans-serif;
$h1FontSize: 2.625rem;
$h1LineHeight: 1.1;
$h1PaddingTop: 20%;

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
    position: relative;
    background: $containerBackground;
     background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-color: #f8f8f8;
    display: flex;
    padding-top: 0;
    padding-bottom: 0;
      margin-right: 0;
    margin-left: 0;
    width: 100%;

    height: auto;
    min-width: 100%;
   
    align-self: flex-end;
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
            font-size:2.188rem;
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

