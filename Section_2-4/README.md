# Section 2

### HTML
    <h1 id="halo">Halo guyss!!!</h1>
    <h2>Apa Kabar</h2>
    <h2>Perkenalkan namaku Anggun</h2>
    <p>Jenis Kelamin :</p>
    <label for="Laki-laki">
        <input type="radio" name="jenisKelamin" value="Laki-laki">Laki-laki
    </label>
    <label for="Perempuan">
        <input type="radio" name="jenisKelamin" value="Perempuan">Perempuan
    </label>
    <button id="submit">Submit</button>
    <p id="output"></p>
    <button id="check">Check getElementsByTagName</button>

### script js
    //getElementById()
    const halo = document.getElementById('halo');
    halo.style.color = 'pink';

    //getElementsByName()
    let button = document.getElementById('submit');
    let output = document.getElementById('output');
    button.addEventListener('click', () => {
        let rates = document.getElementsByName('jenisKelamin');
        rates.forEach((jenisKelamin) => {
            if (jenisKelamin.checked) {
                output.innerText = `Kamu adalah seorang ${jenisKelamin.value}`;
            }
        });
    });

    //getElementsByTagName
    let btn = document.getElementById('check');
    btn.addEventListener('click', () => {
        let tes = document.getElementsByTagName('h2');
        alert(`berapa jumlah tag h2? ${tes.length}`);
    });

# Section 3

### HTML
    <div id="tes">
        <h1>Belajar yuk</h1>
        <h1 class="section3">Ini Section 3</h1>
    </div>
    <div>
        <h2>1. Get the parent element</h2>
        <h2 class="s3">2. Get child elements</h2>
        <h2>3. Get siblings of an element</h2>
    </div>

### script js
    //Get the parent element
    let parentElemen = document.querySelector('.section3')
    parentElemen.style.color = 'blue';

    //Get child elements
    let getChild = parentElemen.getChild;
    let edit = document.getElementById('tes');
    edit.style.color = 'red';

    //Get siblings of an element
    let pilih = document.querySelector('.s3');
    let sibling = pilih.nextElementSibling;
    sibling.style.color = 'pink';

# Section 4

### HTML
    <div id="appendChild">

    </div>

### script js
    //createElement()
    let tambahdiv = document.createElement('div');
    tambahdiv.id = 'tes';
    tambahdiv.innerHTML = '<h1>Ini adalah hasil dari createElement()</h1>';
    document.body.appendChild(tambahdiv);

    //appendChild()
    function buath2(isih2){
        let h2 = document.createElement('h2');
        h2.textContent = isih2;
        return h2;
    }
    const inih2 = document.querySelector('#appendChild');
    inih2.appendChild(buath2('Ini adalah'));
    inih2.appendChild(buath2('hasil dari'));
    inih2.appendChild(buath2('appendChild()'));

    //innerHTML
    let inner = document.createElement('ul')
    inner.innerHTML = '<li>ini adalah contoh</li><li>innerHTML</li>';
    document.body.appendChild(inner);