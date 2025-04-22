<!DOCTYPE html>
<html lang="az">
<head>
    <meta charset="UTF-8">
    <title>Kinoteatr Bilet Sifarişi</title>
    <style>
        body {
            font-family: Arial;
            background-color: #f2f2f2;
            padding: 20px;
        }
        .container {
            width: 400px;
            margin: 0 auto;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px #aaa;
        }
        h2 {
            text-align: center;
            color: #333;
        }
        label {
            display: block;
            margin-top: 10px;
        }
        select, input[type="submit"] {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        #mesaj {
            margin-top: 20px;
            text-align: center;
            color: green;
            font-weight: bold;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Kinoteatr Bilet Sifarişi</h2>
    <form onsubmit="return sifarisiGoster()">
        <label for="film">Film seçin:</label>
        <select id="film" required>
            <option value="">-- Film seçin --</option>
            <option value="Avatar 2">Avatar 2</option>
            <option value="Qara Pantera">Qara Pantera</option>
            <option value="Oppenheimer">Oppenheimer</option>
        </select>

        <label for="seans">Seans vaxtı:</label>
        <select id="seans" required>
            <option value="">-- Seans seçin --</option>
            <option value="11:00">11:00</option>
            <option value="14:00">14:00</option>
            <option value="17:00">17:00</option>
            <option value="20:00">20:00</option>
        </select>

        <label for="yer">Oturacaq nömrəsi:</label>
        <select id="yer" required>
            <option value="">-- Oturacaq seçin --</option>
            <option value="A1">A1</option>
            <option value="A2">A2</option>
            <option value="B1">B1</option>
            <option value="B2">B2</option>
        </select>

        <input type="submit" value="Bileti Sifariş Et">
    </form>

    <div id="mesaj"></div>
</div>

<script>
    function sifarisiGoster() {
        const film = document.getElementById("film").value;
        const seans = document.getElementById("seans").value;
        const yer = document.getElementById("yer").value;

        const mesaj = `"${film}" filmi üçün ${seans} seansına ${yer} oturacağına bilet sifariş etdiniz.`;
        document.getElementById("mesaj").textContent = mesaj;

        return false; // formun göndərilməsinin qarşısını alır
    }
</script>

</body>
</html>
