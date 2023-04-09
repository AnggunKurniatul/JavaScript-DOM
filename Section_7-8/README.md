# Section 7

## Usecase 1

### HTML
    <button id="button">Klik disini dong</button>

### script js
    //JavaScript Events
    let btn = document.querySelector('#button');

    btn.addEventListener('click',function() {
        alert('Terima Kasih');
    });

    //JavaScript Page Load Events
    addEventListener('load', (event) => {
        console.log('The page is fully loaded.');
    });

## Usecase 2

### HTML
    <button id="button">Klik Disini!</button>
    <div id="scroll">
        <p>scroll</p>
    </div>

    <div id="buttonScroll">
        <button id="scrollRight">Scroll Right</button>
        <button id="scrollDown">Scroll Down</button>
    </div>

### CSS
    #button{
        margin-bottom: 20px;
    }
    #scroll {
        height: 200px;
        width: 200px;
        overflow: auto;
        background-color: gray;
    }

    #scroll p {
        height: 300px;
        width: 300px;
    }

### script js
    //JavaScript DOMContentLoaded
    let button = document.getElementById('button');
    button.addEventListener('click', (e) => {
        console.log('button telah di klik');
    });

    //JavaScript Scroll Events
    let control = document.querySelector('#buttonScroll');

    control.addEventListener('click', function (e) {
        let contentScroll = document.getElementById('scroll');
        let button = e.target;
        switch (button.id) {
            case 'scrollRight':
                contentScroll.scrollLeft += 20;
                break;

            case 'scrollDown':
                contentScroll.scrollTop += 20;
                break;
        }
    });