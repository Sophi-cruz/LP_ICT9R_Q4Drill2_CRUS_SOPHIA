<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drill 2 Navbar</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"rel="stylesheet">  
</head>
<body>


<nav class="navbar navbar-expand-sm navbar-dark bg-dark">

        <button class="navbar-toggler" type="button"data-bs-toggle="collapse" data-bs-target="#mynavbar">
            <span class="navbar-toggler-icon"></span>
        </button>

    <div class="collapse navbar-collapse" id="mynavbar">
        <ul class="navbar-nav me-auto">
            <li class="nav-item"> 
                <a class="nav-link" href="index.html" target="_self"> HOME </a>
            </li>

            <li class="nav-item"> 
                <a class="nav-link" href="about.html" target="_self"> ABOUT </a>
            </li>

        </ul>

        <form class="d-flex">
                <input class="form-control me-2" type="text" placeholder="Search">
            <button class="btn btn-primary" type="button"> SEARCH </button>
        </form>

        </div>
    </div>
</nav>


            <br>
        <br>

   <table class="table"> 
  <thead> 
    <tr> 
            <th scope="col">Temperatur</th> 
      <th scope="col">Humidt</th> 
      <th scope="col">Heat index Range</th>
                <th scope="col">Status/Description</th>
    </tr> 
        </thead> 
 
  <tbody> 
    <tr> 
            <th scope="row">20-24</th> 
            <th> 30 - 50 </th>
                          <td> < 27</td> 
                        <td>Comfortable/ Cool</td> 
    </tr> 
        <tr>    
            <th scpoe="row">25 - 27</th> 
                <th>40 - 60</th> 
                            <td>28 - 32</td>
                         <td>Warm</td>
                        
    </tr> 
        <tr> 
            <th scope="row">28 - 31</th> 
                <th>50 - 70</th> 
                        <td>38 - 41</td>
                        <td>Hot</td>
    </tr> 
        <tr> 
            <th scope="row">32 - 35</th> 
                <th> 60 - 80 </th> 
                        <td>38 - 41</td>
                        <td>Very Hot / Caution</td> 
    </tr> 
        <tr>
            <th scope="row">36+</th> 
                <th>70 - 100</th> 
                        <td>> 42</td> 
                        <td>Extreme hot/ danger</td>
    </tr> 
  </body> 
</table> 

<br>

<style>
    body{
        font-family:'Courier New', Courier, monospace;
        text-align: center;
        margin-top: 80px;
        background-color:rgb(97, 97, 97) ;
    }

    .container{
        background: rgb(255, 255, 255);
        padding: 20px;
        width: 300px;
        margin: auto;
        border: 1px solid #c11717;
    }

    input{
        padding: 6px;
        width:80%;
        margin-bottom: 10px;
    }

    button {
        background:rgb(224, 178, 50);
        padding: 8px 15px;
    }

    output {
        margin-top: 15px;
        text-align: left;
    }


</style>


    <div class="container">
        <h2> Heat index </h2>

        <input type="number" id="score" placeholder="Ender Score">
        <br>

        <button onclick="evaluateScore()">EVALUATE</button>

            <div class="output">
                     <p id="status"> </p>
                    <p id="grade"> </p>
              </div>

     </div>

<script>
        function evaluateScore()
         {
            var score = document.getElementById("score").value;

            if(score=== ""){
                alert("Please enter a score.");
                return;
            }

            score = Number(score);
            var status = "";

            if(score >= 0){
                status = "Status";
            }else{
                status = "Status: Discounted eletricity rates";
            }

                var grade = ""
                if(score>="100"){
                    grade="A";
                }else if(score>=80){
                    grade="B";
                }else if(score>=60){
                    grade="C";
                }else{
                    grade="F"; 
                }

                var remark = "";
                switch(grade){
                case "A":
                remark="Extreme hot"
                break;

                case "B":
                remark="Very hot"
                break;

                case "C":
                remark="Hot"
                break;

                case "F":
                remark="warm and cool"
                break;
                }

                document.getElementById("status").innerHTML = status;
                document.getElementById("grade").innerHTML ="Grade: " + grade + " " + remark;

            }

     </script>


</head> 
<body>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
