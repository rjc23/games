<template>
<div>
    <div class="wrapper">
        <div id="stars"></div>
        <div id="stars2"></div>
        <div id="stars3"></div>
        <div id="title">
        <div class="header">
            <h1>
                <span class="games">GAMES.</span>ryancarmody
            </h1>
        </div>
        <br/>
        </div>
    </div>
</div>
</template>

<script>
export default {
    
}
</script>
<style lang="scss">
    // n is number of stars required
    @function multiple-box-shadow ($n) {
    $value: '#{random(2000)}px #{random(2000)}px #f87575';
    @for $i from 2 through $n {
        $value: '#{$value} , #{random(2000)}px #{random(2000)}px #FFF';
    }

    @return unquote($value);
    }
    $shadows-small: multiple-box-shadow(700);
    $shadows-medium: multiple-box-shadow(200);
    $shadows-big: multiple-box-shadow(100);

    .wrapper {
    height: 300px;
    background: radial-gradient(ellipse at bottom, #1B2735 0%, #00334a 100%);
    overflow: hidden;
    box-shadow: 5px 5px 50px 1px rgba(0,0,0,0.5);
    }
    button {
        z-index: 10;
        color: black;
    }
    .header {
        width: 100%;
        height: 300px;
        display: flex;
        justify-content: center;
        align-items: center;
        h1 {
            z-index: 5;
            color: white;
            font-family: 'Inter';
            font-weight: 900;
            font-size: 56px;
            text-shadow: 2px 2px 20px rgba(255,255,255,0.40);
            .games {
                background: -webkit-linear-gradient(315deg,#f87575 25%,#647eff);
                background-clip: text;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;            
            }
        }
    }
    #stars {
    width: 1px;
    height: 1px;
    background: transparent;
    box-shadow: $shadows-small;
    animation: animStar 50s linear infinite;

    &:after {
        content: " ";
        position: absolute;
        top: 2000px;
        width: 1px;
        height: 1px;
        background: transparent;
        box-shadow: $shadows-small;
    }
    }
    #stars2 {
    width: 2px;
    height: 2px;
    background: transparent;
    box-shadow: $shadows-medium;
    animation: animStar 100s linear infinite;

    &:after {
        content: " ";
        position: absolute;
        top: 2000px;
        width: 2px;
        height: 2px;
        background: transparent;
        box-shadow: $shadows-medium;
    }
    }
    #stars3 {
    width: 3px;
    height: 3px;
    background: transparent;
    box-shadow: $shadows-big;
    animation: animStar 150s linear infinite;

    &:after {
        content: " ";
        position: absolute;
        top: 2000px;
        width: 3px;
        height: 3px;
        background: transparent;
        box-shadow: $shadows-big;
    }
    }
    @keyframes animStar {
    from {
        transform: translateY(0px);
    }
    to {
        transform: translateY(-2000px);
    }
    };
</style>