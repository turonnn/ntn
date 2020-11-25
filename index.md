<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato:400,700|Montserrat:900">
    <title>Document</title>
    <style>

body{
    background-color: white;
}
  
#timer {
  color: #eeeeee;
  text-align: center;
  text-transform: uppercase;
  font-family: 'Lato', sans-serif;
  font-size: .7em;
  letter-spacing: 5px;
}

.days, .hours, .minutes, .seconds {
  display: inline-block;
  padding: 20px;
  width: 100px;
  border-radius: 5px;
}

.days {
  background: #75BDEO;
}

.hours {
  background: #F8D49B;
}

.minutes {
  background: #F8BC9B;
}

.seconds {
  background: #F89B9B;
}

.numbers {
  font-family: 'Montserrat', sans-serif;
  color:  #eeeeee;
  font-size: 4em;
  text-align: center;
}

.white {
  position: absolute;
  background:  #eeeeee;
  height: 85px;
  width: 75px;
  left: 30%;
  top: 2%;
}

.blue {
  position: absolute;
  background:  #75BDEO;
  left: 18%;
  top: 9%;
  height: 65px;
  width: 70px;
 
}

.yellow {
  position: absolute;
  background:  #F8D49B;
  height: 80px;
  width: 80px;
  left: 60%;
  top: 5%;
  
}

.orange {
  position: absolute;
  background:  #F8BC9B;
  height: 80px;
  width: 80px;
  left: 60%;
  top: 5%;
 
 }

.pink {
  position: absolute;
  background:  #F89B9B;
  height: 80px;
  width: 80px;
  left: 60%;
  top: 5%;


}


    </style>
</head>
<body>
    
<div id="timer">

    <div class="days"> 
        <div id="days" class="numbers "> </div>days</div> 
      <div class="hours"> 
        <div  id="hours" class="numbers"> </div>hours</div> 
      <div class="minutes"> 
        <div  id="minutes" class="numbers"> </div>minutes</div> 
      <div   class="seconds"> 
        <div id="seconds" class="numbers"> </div>seconds</div> 
      </div>

</div>

</body>
<script>
    const year = new Date().getFullYear();
const myDate = new Date('Feb 10, 2021 00:00:00');
console.log(myDate);

// countdown
let timer = setInterval(function() {

  // get today's date
  const today = new Date().getTime();

  // get the difference
  const diff = myDate - today;

  // math
  let days = Math.floor(diff / (1000 * 60 * 60 * 24));
  let hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  let minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
  let seconds = Math.floor((diff % (1000 * 60)) / 1000);

  // display
  document.getElementById("days").innerHTML=days
  document.getElementById("hours").innerHTML=hours
  document.getElementById("minutes").innerHTML=minutes
  document.getElementById("seconds").innerHTML=seconds



}, 1);
</script>
</html>
