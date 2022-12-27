
<html>

<head>

    <script>
        function count() {
            beli = document.getElementById("buy").value;
            jual = document.getElementById("sell").value;
            lot = document.getElementById("shares").value;
            document.getElementById("hargabeli").innerHTML = (beli * 100 * lot) + (beli * 100 * lot * 0.1 / 100);
            document.getElementById("hargajual").innerHTML = (jual * 100 * lot) - (jual * 100 * lot * 0.2 / 100);
            document.getElementById("profit3").innerHTML = (jual * 100 * lot) - (jual * 100 * lot * 0.2 / 100) - ((beli * 100 * lot) + (beli * 100 * lot * 0.1 / 100));
            document.getElementById("hargabeli2").innerHTML = (beli * 100 * lot) + (beli * 100 * lot * 0.15 / 100);
            document.getElementById("hargajual2").innerHTML = (jual * 100 * lot) - (jual * 100 * lot * 0.25 / 100);
            document.getElementById("profit4").innerHTML = (jual * 100 * lot) - (jual * 100 * lot * 0.25 / 100) - ((beli * 100 * lot) + (beli * 100 * lot * 0.15 / 100));
        }

    </script>
    <style>
        .containerbox {
            width: 90%;
            height: 350px;

        }

        .column1 {
            float: left;
            width: 50%;
            padding: 20px;
        }


        h2,
        p {
            margin-left: 20px;
            text-align: center;
        }

        #category {
            text-align: left;
            padding: 10px;
            width: 100%;
            flex-direction: row;
            display: flex;

        }

        #col-rev {
            text-align: center;
        }

        #col-rev2 {
            flex-direction: row;
            display: flex;
            width: 40%;
            left: 0;
        }

        #title {
            text-align: left;
            width: 50%;
        }

        label {
            font-weight: bold;
            width: 40%;
            vertical-align: text-top;
            padding: 15px;
        }

        input[type=textcurrency],
        select {
            width: 100%;
            padding: 5px 25px;
            margin: 8px 0px;
            display: inline-block;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        input[type=text],
        select {
            width: 40%;
            padding: 12px 20px;
            margin: 8px 0;
            display: inline-block;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }


        body {
            background: #fafafa;
            font-family: Helvetica, Arial;
        }

        .boxes {
            width: 40%;
            padding: 12px 20px;
            margin: 8px 0;
            display: inline-block;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        .btn {

            left: 0;
            padding: 10px;
            width: 100%;
            margin-bottom: 20px;
            align-items: flex-end;
            justify-content: flex-end;
        }

        input[type=submit] {
            background-color: #04AA6D;
            width: 90%;
            color: white;
            padding: 16px 32px;
            text-decoration: none;
            margin-left: 20px;
            cursor: pointer;
            align-items: center;
            justify-content: center;

        }

        .command {
            flex-direction: row;
            display: flex;
        }

        .boxes {
            border: 1px solid lightgrey;
        }
    </style>


</head>

<body>
    <div class="containerbox">

        <div class="column1">

            <div id="category">
                <label style>Buy</label>
                <input type="text" id="buy" autofocus>
            </div>

            <div id="category">
                <label style>Sell</label>
                <input type="text" id="sell">
            </div>

            <div id="category">
                <label style>Shares</label>
                <input type="text" id="shares" value="100">
            </div>

            <div class="btn">
                <input type="submit" value="Submit" onclick="count()">
            </div>



            <div style="border:1px solid; margin-inline-end: 20px; margin-inline-start: 20px;"></div>

            <div style="border:0.5px solid lightgrey; padding:10px; margin:10px">
                <div style="margin-left:20px">
                    <H3>0.3%</H3>
                </div>

                <div id="col-rev2">
                    <p id="title">Harga Beli</p>
                    <p><span id="hargabeli"></span></p>
                </div>

                <div id="col-rev2">
                    <p id="title">Harga Jual</p>
                    <p><span id="hargajual"></span></p>
                </div>

                <div id="col-rev2">
                    <p id="title">Profit</p>
                    <p><span id="profit3"></span></p>
                </div>
            </div>


            <div style="border:0.5px solid lightgrey; padding:10px; margin:10px">
                <div style="margin-left:20px">
                    <H3>0.4%</H3>
                </div>
                <div id="col-rev2">
                    <p id="title">Harga Beli</p>
                    <p><span id="hargabeli2"></span></p>
                </div>

                <div id="col-rev2">
                    <p id="title">Harga Jual</p>
                    <p><span id="hargajual2"></span></p>
                </div>

                <div id="col-rev2">
                    <p id="title">Profit</p>
                    <p><span id="profit4"></span></p>
                </div>
            </div>










