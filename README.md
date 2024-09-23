<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Buborékrendezés Algoritmus</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Buborékrendezés Algoritmus Bemutatása</h1>
    </header>
    
    <section id="leiras">
        <h2>Algoritmus Leírása</h2>
        <p>A buborékrendezés egy egyszerű rendezési algoritmus, amely többször átnézi az elemek listáját, és az egymás mellett álló elemeket összehasonlítja. Ha az elemek nincsenek megfelelő sorrendben, akkor felcseréli őket. Ezt a folyamatot addig ismétli, amíg az összes elem helyesen nem lesz rendezve.</p>
    </section>

    <section id="hatekony">
        <h2>Hatékonyság és Tárigény</h2>
        <ul>
            <li><strong>Legrosszabb eset:</strong> O(n²)</li>
            <li><strong>Legjobb eset:</strong> O(n)</li>
            <li><strong>Átlagos eset:</strong> O(n²)</li>
            <li><strong>Tárigény:</strong> O(1) – a rendezés helyben történik</li>
        </ul>
    </section>

    <section id="kod">
        <h2>Kód (Python)</h2>
        <pre>
<code>
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if not swapped:
            break
    return arr

arr = [64, 34, 25, 12, 22, 11, 90]
sorted_arr = bubble_sort(arr)
print("Rendezett lista:", sorted_arr)
</code>
        </pre>
    </section>

    <section id="abra">
        <h2>Szemléltető Ábra</h2>
        <img src="bubblesort_diagram.png" alt="Buborékrendezés lépéseinek ábrája">
    </section>

    <section id="forrasok">
        <h2>Források</h2>
        <ul>
            <li><a href="https://www.geeksforgeeks.org/bubble-sort/" target="_blank">GeeksforGeeks</a></li>
            <li><a href="https://en.wikipedia.org/wiki/Bubble_sort" target="_blank">Wikipedia - Bubble Sort</a></li>
            <li><a href="https://www.programiz.com/dsa/bubble-sort" target="_blank">Programiz</a></li>
            <li><a href="https://www.khanacademy.org/computing/computer-science/algorithms" target="_blank">Khan Academy</a></li>
        </ul>
    </section>

    <footer>
        <p>Készítette: [A Te Neved]</p>
    </footer>
</body>
</html>



* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f4f4f4;
    padding: 20px;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

h1 {
    font-size: 2.5rem;
}

section {
    margin-bottom: 20px;
    padding: 15px;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h2 {
    font-size: 1.8rem;
    color: #333;
    margin-bottom: 10px;
}

p, ul, pre {
    font-size: 1rem;
    margin-bottom: 10px;
    color: #555;
}

ul {
    list-style-type: disc;
    padding-left: 20px;
}

pre {
    background-color: #f8f8f8;
    padding: 15px;
    border-radius: 5px;
    overflow-x: auto;
}

code {
    font-family: 'Courier New', Courier, monospace;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: 0 auto;
}

a {
    color: #007bff;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

footer {
    text-align: center;
    margin-top: 20px;
    padding: 10px 0;
    background-color: #333;
    color: #fff;
}
