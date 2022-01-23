# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
### CSS :
~~~
.header {
    width: auto;
    margin-left: auto;
    margin-right: auto;
    border-width: 0px 0px 0px 0px;
    border-style: none;
    background-color: transparent;
    height: auto;
    text-align: center;
    font-size: 20px;
    border: none;
    padding: 20px;
}

.hhh {
    text-align: center;
}

button {
    font-size: 20px;
    background-color: #ffd215;
    color: #343233;
    border: none;
    cursor: pointer;
    text-align: center;
    display: inline-flex;
    border-radius: 20px;
    padding: 20px;
}

.u {
    text-align: center;
}

.container {
    width: 75%;
    margin-left: auto;
    margin-right: auto;
    border-width: 1px 1px 1px 1px;
    border-style: solid;
    border: 1px solid;
    background-color: transparent;
    height: auto;
    text-align: center;
    font-size: 20px;
    border-radius: 20px;
}

.footer {
    width: 75%;
    margin-left: auto;
    margin-right: auto;
    border-width: 1px 1px 1px 1px;
    border-style: solid;
    border: 1px solid;
    background-color: transparent;
    height: auto;
    text-align: center;
    font-size: 20px;
    height: 50px;
    border-radius: 20px;
}

.t {
    background-image: radial-gradient(ellipse closest-side at 50% 50%, #3a3f45, #37383c 25%, #343233);
    color: #efdab9;
    height: 100%;
}

input {
    background-color: transparent;
    font-size: 20px;
    border-radius: 5px;
    border-color: #efdab9;
    color: #efdab9;
    text-align: center;
}
~~~
### HTML :
~~~
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./css/layout1.css" />
    <title>Mathematical Calculations</title>
    <script>
        function volcone() {
            var rc, hc, vc, rc1, hc1;
            var len, reg, res;
            rc = document.getElementById("radcone").value;
            hc = document.getElementById("heightcone").value;
            rc1 = parseInt(rc);
            hc1 = parseInt(hc);
            reg = new RegExp("^[.]?[0-9]+[.]?[0-9]*$");
            res1 = rc.match(reg);
            res2 = hc.match(reg);
            if (res1 == null && res2 == null) {
                alert("Please enter the radius and height")
            } else if (res1 == null) {
                alert("Please enter the valid radius!");
            } else if (res2 == null) {
                alert("Please enter the valid height!")
            } else {
                vc = (rc1 ** 2) * hc1 * 22 / (7 * 3);
                document.getElementById("vol_cone").innerHTML = "Volume Of Cone : " + vc + " cubic meter";
            }
        }

        function volcylinder() {
            var rcy, hcy, vcy, rcy1, hcy1;
            var len, reg, res;
            rcy = document.getElementById("radcylinder").value;
            hcy = document.getElementById("heightcylinder").value;
            rcy1 = parseInt(rcy);
            hcy1 = parseInt(hcy);
            reg = new RegExp("^[.]?[0-9]+[.]?[0-9]*$");
            res1 = rcy.match(reg);
            res2 = hcy.match(reg);
            if (res1 == null && res2 == null) {
                alert("Please enter the radius and height")
            } else if (res1 == null) {
                alert("Please enter the valid radius!");
            } else if (res2 == null) {
                alert("Please enter the valid height!")

            } else {
                vcy = (rcy1 ** 2) * hcy1 * 22 / 7;
                document.getElementById("vol_cylinder").innerHTML = "Volume Of Cylinder : " + vcy + " cubic meter";
            }
        }
    </script>
</head>

<body>
    <div class="t">
        <div class="header">
            <h1>MATHEMATICAL CALCULATIONS</h1>
        </div><br>
        <div class="container">
            <div class="ee">
                <h2 class="hhh">Volume Of Cone</h2>
                <label for="radcone">Radius Of Cone:</label>
                <input type="text" name="radcone" id="radcone"><label> in meter</label><br><br>
                <label for="heightcone">Height Of Cone:</label>
                <input type="text" name="heightcone" id="heightcone"><label> in meter</label><br><br>
                <button type="button" onclick="volcone()">Calculate</button><br><br>
                <label class="u">Volume of Cone = (πr^2h)/3</label><br><br>
                <label class="u" id="vol_cone"></label>
            </div>

            <div class="ee">
                <h2 class="hhh">Volume Of Cylinder</h2>
                <label for="radcylinder">Radius Of Cylinder:</label>
                <input type="text" name="radcylinder" id="radcylinder"> <label>  in meter</label><br><br>
                <label for="heightcylinder">Height Of Cylinder:</label>
                <input type="text" name="heightcylinder" id="heightcylinder"><label>  in meter</label><br><br>
                <button class="f" type="button" onclick="volcylinder()">Calculate</button><br><br>
                <label class="u">Volume of Cylinder = πr^2h</label><br><br>
                <label class="u" id="vol_cylinder"></label>
            </div>
        </div><br>
        <div class="footer">Developed by Venkatesh E</div>
    </div>
</body>

</html>
~~~
## OUTPUT:
![webpage](calculations/static/img/1.jpg)
## Result:

Thus a website is designed to perform mathematical calculations in the client side.
# HTML Canvas Experiment:
## Program:
~~~
<!DOCTYPE html>
<html>
<title>Canvas</title>

<body>
    <h1 style="text-align: center;">Assignment</h1>
    <canvas id="mycanvas" width="600px" height="400px" style="border:2px solid #000000">
        </canvas>
    <script>
        var canvas = document.getElementById("mycanvas");
        var ctx = mycanvas.getContext("2d");
        ctx.moveTo(5, 5);
        ctx.lineWidth = 6;
        ctx.lineTo(590, 390);
        ctx.stroke();
        ctx.fillStyle = "#FF0000";
        ctx.fillRect(5, 5, 590, 390);
        ctx.stroke();
        ctx.fillStyle = "#000000";
        ctx.font = "900 30px Arial";
        ctx.fillText("DANGER", 20, 370);
    </script>

    <canvas id="canvas" width="400px" height="400px" style="border:2px solid #000000">
        </canvas>
    <script>
        var canvas = document.getElementById("canvas");
        var ctx = canvas.getContext("2d");
        ctx.beginPath();
        ctx.arc(200, 200, 150, 100, -1.5 * Math.PI, true);
        ctx.strokeStyle = "black";
        ctx.lineWidth = 4;
        ctx.fillStyle = "lightgreen";
        ctx.fill();
        ctx.stroke();
        ctx.beginPath();
        ctx.arc(160, 160, 20, 25, -1.5 * Math.PI, true);
        ctx.fillStyle = "lightblue";
        ctx.fill();
        ctx.stroke();
        ctx.beginPath();
        ctx.arc(235, 160, 20, 10, -1.5 * Math.PI, true);
        ctx.fillStyle = "lightblue";
        ctx.fill();
        ctx.stroke();
        ctx.beginPath();
        ctx.arc(200, 195, 122, 1 * Math.PI, 2 * Math.PI, true);
        ctx.strokeStyle = "violet";
        ctx.lineWidth = 4;
        ctx.stroke()
    </script>
</body>

</html>
~~~
## Output:
![output](calculations/static/img/2.jpg)
## Result:

Thus a website is designed with Canvas
