For the first task: i choose poster number 2. i started by extracting and simplyfing arches and paths for objects to make the code as minimal as possible. I used *simplify* on object to decrease PTS by playing with simplify curve, the elements do change thir original form, but they still remain almost the same as from the begining of just ith less detialed sharpness on the corners for instance. Reasoning for that as mentioned is to make SVG code as litlle as possible and only take the parts that are nescassery. I found that exporting them directly as SVG did not worked for me that well, so I found on YT another tutorial as on how to export each element as an assest (which can be done in illustatror). tutorial can be foudn here:
     https://www.youtube.com/watch?v=SggOgHs4eyg

For task two implementaiton of poster by using HTML and CSS: i started by created the background layout wich contianed by 7 main SVG elements - the wave in different colors elements. And i used absolute - positioing and viewport units to diplay them in the middle, as well as z-index to some of the can be placed on top or underenath eachother. As for media queries for smaller screens, we wanted to achieve the look of seing the poster in full view, so we gave to the body margin:0 and padding:0. We also saw after exporting text-content from poster that the code was really long, even after simplifying it. What we did instead was to download quite similar font and use <p> - paragrahs instead, which would take up much less of script in HTLM. As for the header wirth colors green and blue we used it as an SVG since script was 



teskt for meg selv -------------
body {
    background-color: rgb(249, 249, 242);
  }
  main {
    width: 100%; 
    box-sizing: border-box; 
    padding: 2px; 
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .svg-container {
    border: 2px solid red;
    position: relative;
    width: 40vw; 
    height: 100vh; 
    min-width: 500px; 
    min-height: 500px; 
    overflow: auto;
    margin: 0;
  }

  .svg-element {
    position: absolute;
    width: 100%; /* Adjust based on aspect ratio */
    max-width: 100%;
    display: block;
    height: auto; /* Make SVG fully fill container height */
    /*left: 50%; /* Center horizontally */
    /*transform: translate(-50%, -50%); /* Center the element */
}

#layer__white {
  fill: #fff;
}
#layer__blue1 {
    fill: #035ca7;
    z-index: -1;
}
#layer__blue--transperant{
    fill: #04b1dc;
    isolation: isolate;
    opacity: .15;
    z-index: -2;
    top: 9rem;
}
#layer__orange {
    fill: #c87161;
    isolation: isolate;
    opacity: .38;
    top: 25.6rem;
}
#earth__blue{
    fill: #04b1dc;
    top: 30rem;
} 
#earth__patch{
    fill: #a1cf6d;
    top: 30rem;
}

#earth__blue,
#earth__patch{
  stroke-miterlimit: 10;
  stroke: #231f20;
  stroke-width: 4.6px;
}

@media screen and (max-width: 600px) {
/* Ensure the parent container allows for proper layout */
main {
  width: 100%; /* Use full width of the viewport */
  box-sizing: border-box; /* Include padding and border in the element's total width and height */
  padding: 2px; /* Example padding, adjust as needed */
}

.svg-container {
  width: 100%; 
  min-width: auto; 
  height: auto; 
  overflow: visible; 
}


.svg-element {
    max-width: 100%; 
}

#layer__white {
  top: 1%;
}
#layer__blue1 {
   top: 4%;
   z-index: -1;
}
#layer__blue--transperant {
    top: 20%; 
}

#layer__orange {
    top: 51%;
}

#earth__blue,
#earth__patch {
    top: 59%; 
}
}



/////////////////////////// 
main {
  width: 100%; 
  box-sizing: border-box; 
  padding: 2px; 
  display: flex;
  justify-content: center;
  align-items: center;
}
.svg-container {
  border: 2px solid red;
  position: relative;
  width: 40%; 
  height: 100vh; 
  min-width: 500px; 
  min-height: 500px; 
  overflow: auto;
  margin: 0;
}

.svg-element {
  position: absolute;
  width: 100%; /* Adjust based on aspect ratio */
  max-width: 100%;
  display: block;
  height: auto; /* Make SVG fully fill container height */
  /*left: 50%; /* Center horizontally */
  /*transform: translate(-50%, -50%); /* Center the element */
}


//////////
/*@media screen and (max-width: 600px) {
/* Ensure the parent container allows for proper layout */
/*main {
width: 100%; 
box-sizing: border-box; 
padding: 2px; 
}

.svg-container {
width: 100%; 
min-width: auto; 
height: auto; 
overflow: visible; 
}


.svg-element {
  max-width: 100%; 
}

#layer__white {
top: 1%;
}
#layer__blue1 {
 top: 4%;
 z-index: -1;
}
#layer__blue--transperant {
  top: 20%; 
}

#layer__orange {
  top: 51%;
}

#earth__blue,
#earth__patch {
  top: 59%; 
}
}*/