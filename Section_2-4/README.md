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