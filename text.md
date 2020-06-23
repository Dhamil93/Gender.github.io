<!DOCTYPE html>
<html>

<head>

    <title>
        Ordering System
    </title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

</head>
<style>
    p   {
        text-align: center;
        font-weight: bolder;
        color: blue;
    }
    h4 {
        color: blue;
        font-weight: bold;
    }

</style>

<body>
    <p>
        Select a radio button and click on Submit to know where you belong according to your age.
    </p>

    <h4>Gender:</h4>
    <input type="radio" name="Gender" value="Female">Female
    <input type="radio" name="Gender" value="Male">Male
    <input type="radio" name="Gender" value="Other">Other

    <br>

    <h4>Age-Range:</h4>
    <input type="radio" name="Age" value="18-25">18-25
    <input type="radio" name="Age" value="26-30">26-30
    <input type="radio" name="Age" value="31-40">31-40
    <input type="radio" name="Age" value="31-40">41-50+

    <br>

    <h4>Floor:</h4>
    <input type="radio" name="Floors" value="3rd Floor">3rd Floor
    <input type="radio" name="Floors" value="2nd Floor">2nd Floor
    <input type="radio" name="Floors" value="1st Floor">1st floor
    <input type="radio" name="Floors" value="Ground Floor">Ground Floor
    <br>


    <button type="button" onclick="displayRadioValue()">
        Submit
    </button>

    <br>

    <div id="result"></div>

    <script>
        function displayRadioValue() {
            document.getElementById("result").innerHTML = "";
            var ele = document.getElementsByTagName('input');

            for (i = 0; i < ele.length; i++) {

                if (ele[i].type = "radio") {

                    if (ele[i].checked)
                        document.getElementById("result").innerHTML
                            += ele[i].name + " Value: "
                            + ele[i].value + "<br>";
                }
            }
        } 
    </script>
</body>

</html>
