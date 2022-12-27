<!DOCTYPE html>
<html>

<head>

    <script>
        function count() {
            start = document.getElementById("start").value;
            end = document.getElementById("end").value;
            const dateOne = new Date(start);
            const dateTwo = new Date(end);
            const time = Math.abs(dateTwo - dateOne);
            const days = Math.ceil(time / (1000 * 60 * 60 * 24))
            const hours = Math.ceil(time / (1000 * 60 * 60 * 24) * 24)
            const minutes = Math.ceil(time / (1000 * 60 * 60 * 24) * 24 * 60)
            const seconds = Math.ceil(time / (1000 * 60 * 60 * 24) * 24 * 60 * 60)
            document.getElementById("days").innerHTML = days;
            document.getElementById("hours").innerHTML = hours;
            document.getElementById("minutes").innerHTML = minutes;
            document.getElementById("seconds").innerHTML = seconds;

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
            width: 50%;
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


        input[type=submit] {
            background-color: #04AA6D;
            width: 100px;
            border: none;
            color: white;
            padding: 16px 32px;
            text-decoration: none;
            margin: 4px 2px;
            cursor: pointer;
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
                <label style>Begin Date</label>
                <input type="date" id="start" name="trip-start">
            </div>

            <div id="category">
                <label style>End Date</label>
                <input type="date" id="end" name="trip-end">
            </div>

            <input type="submit" value="submit" onclick="count()">



            <div style="border:1px solid; margin-inline-end: 20px; margin-inline-start: 20px;"></div>
            <div id="col-rev2">
                <p id="title">Number of Days</p>
                <p><span id="days"></span> Days</p>
            </div>
            <div id="col-rev2">
                <p id="title">Number of Hours</p>
                <p><span id="hours"></span> Hours</p>
            </div>
            <div id="col-rev2">
                <p id="title">Number of Minutes</p>
                <p><span id="minutes"></span> Minutes</p>
            </div>
            <div id="col-rev2">
                <p id="title">Number of Seconds</p>
                <p><span id="seconds"></span> Seconds</p>
            </div>











</body>

</html>
