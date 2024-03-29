# Design
```
<!DOCTYPE html>
<html lang="ru">
<head>
    <title>Design</title>
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=0.86, maximum-scale=3.0, minimum-scale=0.86">
    <script src="/static/html/components/component_modules/mocha/mocha.js" defer></script>
    <link rel="stylesheet" href="/static/html/components/component_modules/mocha/mocha.css" media="print" onload="this.media='all'">
    <script src="/static/html/components/component_modules/eruda/eruda.js" defer></script>
    <meta property="og:site_name" content="design"/>
    <meta property="og:locale" content="ru_RU"/>
    <meta property="og:type" content="contract"/>
    <meta property="og:title" content="design"/>
    <meta property="og:description" content="design"/>
    <meta property="og:url" content="https://zababurinsv.github.io/design/"/>
    <meta property="og:image" content="https://i.imgur.com/pSrPUkJ.jpg"/>
    <meta property="og:image:width" content="537"/>
    <meta property="og:image:height" content="240"/>
    <style>
        @font-face {
            font-family: 'GothamPro';
            src: url('/css/GothamPro/GothamPro.eot');
            src: url('/css/GothamPro/GothamPro.eot?#iefix') format('embedded-opentype'),
            url('/css/GothamPro/GothamPro.woff') format('woff'),
            url('/css/GothamPro/GothamPro.ttf') format('truetype');
            font-weight: normal;
            font-style: normal;
        }

        @font-face {
            font-family: 'GothamPro-Bold';
            src: url('/css/GothamPro-Bold/GothamPro-Bold.eot?') format('eot'),
            url('/css/GothamPro-Bold/GothamPro-Bold.otf')  format('opentype'),
            url('/css/GothamPro-Bold/GothamPro-Bold.woff') format('woff'),
            url('/css/GothamPro-Bold/GothamPro-Bold.ttf')  format('truetype'),
            url('/css/GothamPro-Bold/GothamPro-Bold.svg#GothamPro-Bold') format('svg');
        }
    </style>
<!--    <script src="https://www.google.com/recaptcha/api.js?render=6LePTtIZAAAAANZeZsg3q5to7XxktI7XE4l9W5Fo"></script>-->
</head>
<body>
<script>
    document['body']['attachShadow']({mode: 'open'});
    let spinner = document.createElement('img')
    spinner.src = '/images/spinner.gif'
    spinner.style.display = 'flex'
    spinner.style.margin = 'auto'
    spinner.style.justifyContent = 'center'
    spinner.style.paddingTop = '25%'
    document['body']['shadowRoot'].appendChild(spinner)
</script>

<section id="template" slot="body">
    <div id="components">
        <varan-header preset="index"></varan-header>
<!--        <waves-modal></waves-modal>-->
        <image-index>
<!--            <web3-google>-->
<!--                <varan-editor type="swap">-->
<!--                    <varan-modal-button  type="swap"  mode="view"></varan-modal-button>-->
<!--                    <varan-menu type="light-editor"  slot="edit"></varan-menu>-->
<!--                </varan-editor>-->
<!--                <codemirror-main></codemirror-main>-->
<!--                <directory-list></directory-list>-->
<!--            </web3-google>-->
        </image-index>
    </div>
<!--    <div id="info">-->
<!--        Console-->
<!--        <div class="container">-->
<!--            <input type="button" value="erase" id="erase">-->
<!--            <input type="button" value="help" id="help">-->
<!--            <varan-menu preset="deals"></varan-menu>-->
<!--        </div>-->
<!--    </div>-->
<!--    <div id="tests">-->
<!--        <ul id="mocha"></ul>-->
<!--    </div>-->
    <varan-footer preset="index"></varan-footer>
</section>
</body>
<script type="text/javascript" src="/distrib/fs/fs.js"></script>
<script type="module" src="/static/html/components/varan-header/varan-header.mjs" async></script>
<script type="module" src="/static/html/components/varan-footer/varan-footer.mjs" async></script>
<script type="module" src="/static/html/components/waves-modal/waves-modal.mjs" async></script>
<script type="module" src="/static/html/components/varan-menu/varan-menu.mjs" async></script>
<script type="module" src="/static/html/components/image-index/image-index.mjs" async></script>
<script type="module">
    import tests from  '/static/html/components/component_modules/tests/tests.mjs'
    // grecaptcha.ready(function() {
    //
    //     grecaptcha.execute('6LePTtIZAAAAANZeZsg3q5to7XxktI7XE4l9W5Fo', {action: 'homepage'})
    //         .then(function(token) {
    //
    //     console.log('capcha',token)
    //
    //     });
    //
    // });
    window.onload = () =>{
        function views() {
            let slot = document.createElement('slot')
            slot.name="body"
            document['body']['shadowRoot'].querySelector('img').remove()
            document['body']['shadowRoot'].appendChild(slot)
        }
        setTimeout(views, 1000);
    }
    // eruda.init();
    let setup =  mocha.setup('bdd')
    tests()
</script>
<style>
    :root {
        --width: 100%;
        --height: 100%;
    }
    #mocha-report{
        font-size: 2.5vw;
    }
    #mocha-report > li > ul > li > h2{
        font-size: 2vw;
    }

    div#tests {
        padding: 0.4vw;
    }
    ul#mocha-stats > li.progress > canvas{
        background: #cdcdcd;
        border-radius: 50%;
    }
    ul#mocha-stats{
        position: absolute;
        background: black;
        border-radius: 0.5vw;
        display: flex;
        color: white;
        font-size: 2vw;
        align-items: center;
        box-sizing: border-box;
        padding: 1vw;
        top: auto;
        margin-top: 1.5vw;
    }
    ul#mocha-stats > li{
        padding: 0;
        box-sizing: border-box;
    }
    ul#mocha-stats > li.progress{
        display: flex;
    }
    #mocha-report > li > ul > li.suite > ul > li > h2{

        font-size: 1.8vw;
    }
    ul#mocha-stats > li.passes > em, ul#mocha-stats > li.failures > em, ul#mocha-stats > li.duration > em{
        color: white;
    }
    p{
        justify-content: center;

    }
    a{
        text-decoration: none;
        color: tomato;
    }
    div#components{
        display: flex;
        flex-direction: row;
        height: var(--height);
        flex-wrap: wrap;
        margin: auto;
        justify-content: space-evenly;
        align-items: center;
    }
    header{
        text-align: center;
        font-size: 5vw;
    }
    varan-header{
        width: 100%;
    }
    p{
        margin: 0;
    }
    div#name, div#address, div#account, div#runmethod {
        display: flex;
        flex-direction: column;
        justify-content: center;
        box-shadow: inset 0vw 0vw 1vw 0px #7694f4;
        box-sizing: border-box;
        padding: 2vw;

        text-align: center;
    }
    input.help,  input.time,  input.last,  input#erase, input#help{
        cursor: pointer;
    }
    input.name, input.address, input.account, input.help, input.runmethod,  input.time,  input.last,input#help,  input#erase{
        align-self: center;
        display: flex;
        box-sizing: border-box;
        padding: 1vw;
        flex-direction: row;
        width: 37vw;
        border: .1vw solid #acb2b5;
        border-radius: 0.5vw;
        margin: auto;
        margin: 1vw;
        outline: none;
        justify-content: space-around;
        font-size: 3vw;
        color: steelblue;
    @include fonts(8);
        font-family: Roboto,serif;
        /*color: #acb2b5;*/
        background: transparent;
    }
    label.name, label.address, label.account, div.container, label.runmethod{
        display: flex;
        align-self: center;
        box-sizing: border-box;
        padding: 1vw;
        flex-direction: row;
        width: 37vw;
        border: .1vw solid #acb2b5;
        border-radius: 0.5vw;
        margin: auto;
        margin-top: 1vw;
        margin-bottom: 1vw;
        outline: none;
        justify-content: center;
    //height: 5vw;
    @include fonts(8);
        font-family: Roboto,serif;
        color: #acb2b5;
        background: transparent;
        cursor: pointer;
    }
    div#info{
        color: red;
        box-shadow: inset 0vw 0vw 1vw 0px #7694f4;
        padding: 2vw;
        box-sizing: border-box;
        text-align: center;
        width: 99%;
        background: white;
        margin: auto;
        margin-top: 1.2vw;
        margin-bottom: 1.2vw;
        display: flex;
        justify-content: center;
        flex-direction: column;
        border-radius: 0.4vw;
    }
    div{
        word-wrap: break-word;
        white-space: normal;
    }
    ul#mocha{
        color: #348a00;
        position: relative;
        overflow: scroll;
        height: 50vw;
        box-sizing: border-box;
        text-align: left;
        border-radius: .4vw;
        box-shadow: inset 0vw 0vw 1vw 0px #7694f4;
        font-family: Roboto,serif;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        /*padding: 2vw;*/
        overflow-x: hidden;
        /*overflow-y: hidden;*/
        white-space: pre-wrap;
        margin: 0;
    }
    div.container{
        width: 100%;
        margin: 1vw;
    }

</style>
</html>
```