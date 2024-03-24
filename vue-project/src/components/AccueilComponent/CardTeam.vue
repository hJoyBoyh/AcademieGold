<script>

</script>
<template>
    <div class="card">
       
        <div class="content">
            
          <div class="back">
            <div class="back-content">
             
              <img src="../../assets/hayetImg.png" alt="">
            </div>
          </div>
          <div class="front">
            
            <div class="img">
              <div class="circle">
              </div>
              <div class="circle" id="right">
              </div>
              <div class="circle" id="bottom">
              </div>
            </div>
      
            <div class="front-content">
              
              <div class="description">
                <div class="title">
                  <p class="title">
                    <strong>Hayet Drareni</strong>
                  </p>
                </div>
                <p class="card-footer">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Neque laoreet suspendisse interdum consectetur. Faucibus a pellentesque sit amet porttitor. Ut lectus arcu bibendum at varius vel pharetra. Mattis vulputate enim nul
                </p>
                
              </div>
              
            </div>
            
          </div>
         
        </div>
        <h2>Hayet Drareni</h2>
      </div>

</template>
<style scoped>
h2{
    text-align: center;
    color: white;

}
img{
    height: 100%;
    width: 100%;
}
.card {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

    overflow: visible;
    width: 290px;
    height: 354px;
  }
  
  .content {
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    transition: transform 300ms;
    box-shadow: 0px 0px 10px 1px #000000ee;
    border-radius: 5px;
  }
  
  .front, .back {
    background-color: #151515;
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    -webkit-backface-visibility: hidden;
    border-radius: 5px;
    overflow: hidden;
  }
  
  .back {
    width: 100%;
    height: 100%;
    justify-content: center;
    display: flex;
    align-items: center;
    overflow: hidden;
  }
  
  .back::before {
    position: absolute;
    content: ' ';
    display: block;
    width: 160px;
    height: 160%;
    background: linear-gradient(90deg, transparent, #CFA246, #CFA246, #CFA246, #CFA246, transparent);
    animation: rotation_481 5000ms infinite linear;
  }
  
  .back-content {
    position: absolute;
    width: 99%;
    height: 99%;
    background-color: #151515;
    border-radius: 5px;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 30px;
  }
  
  .card:hover .content {
    transform: rotateY(180deg);
  }
  
  @keyframes rotation_481 {
    0% {
      transform: rotateZ(0deg);
    }
  
    0% {
      transform: rotateZ(360deg);
    }
  }
  
  .front {
    transform: rotateY(180deg);
    color: white;
    border:  2px solid #CFA246;
  }
  
  .front .front-content {
    position: absolute;
    width: 100%;
    height: 100%;
   
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .front-content .badge {
    background-color: #00000055;
    padding: 2px 10px;
    border-radius: 10px;
    backdrop-filter: blur(2px);
    width: fit-content;
  }
  
  .description {
    box-shadow: 0px 0px 10px 5px #00000088;
    width: 100%;
    height: 100%;
    padding: 0px;
    background-color: #00000099;
    backdrop-filter: blur(5px);
    border-radius: 5px;
    text-align: center
  }
  
  .title {
    font-size: 1.5em;
    max-width: 100%;
    display: flex;
    justify-content: center;
    text-align: center;
    color: #CFA246;
  }
  
  .title p {
    width: 50%;
    
  }
  
  .card-footer {
    height: 80%;
    color: #ffffff88;
    margin-top: 5px;
    font-size: 1em;
    text-align: center;
    padding: 5px;
  }
  
  .front .img {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
  }
  
  .circle {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background-color: #ffbb66;
    position: relative;
    filter: blur(15px);
    animation: floating 2600ms infinite linear;
  }
  
  #bottom {
    background-color: #ff8866;
    left: 50px;
    top: 0px;
    width: 150px;
    height: 150px;
    animation-delay: -800ms;
  }
  
  #right {
    background-color: #ff2233;
    left: 160px;
    top: -80px;
    width: 30px;
    height: 30px;
    animation-delay: -1800ms;
  }
  
  @keyframes floating {
    0% {
      transform: translateY(0px);
    }
  
    50% {
      transform: translateY(10px);
    }
  
    100% {
      transform: translateY(0px);
    }
  }
</style>