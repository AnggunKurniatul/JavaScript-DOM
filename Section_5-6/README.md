# Section 5

### HTML
    <p>klik button di bawah ini untuk menuju ke materi JavaScript DOM</p>
    <button>
        <a id="btn">JavaScript DOM</a>
    </button>
    <button>
        <a id="btn2" href="https://www.javascripttutorial.net/javascript-dom/">JavaScript DOM</a>
    </button>

### script js
    //setAttribute() 
    let buttonJSDOM = document.querySelector('#btn');
    if (buttonJSDOM) {
        buttonJSDOM.setAttribute('href', 'https://www.javascripttutorial.net/javascript-dom/');
    }

    //removeAttribute()
    let button2 = document.querySelector('#btn2');
    if (button2){
        button2.removeAttribute('href');
    }

# Section 6

### HTML
    <h1 id="check" class="check">Ini contoh getComputedStyle()</h1>

### CSS
    .check {
        color: pink;
    }

### script js
    //getComputedStyle
    let check = document.querySelector('.check');
    let style = getComputedStyle(check);

    console.log('color:', style.color);

    //className property
    let p = document.querySelector('#check');
    console.log(p.className);