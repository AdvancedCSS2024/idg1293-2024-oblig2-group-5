For the first task: i choose poster number 2. i started by extracting and simplyfing arches and paths for objects to make the code as minimal as possible. I used *simplify* on object to decrease PTS by playing with simplify curve, the elements do change thir original form, but they still remain almost the same as from the begining of just ith less detialed sharpness on the corners for instance. Reasoning for that as mentioned is to make SVG code as litlle as possible and only take the parts that are nescassery. I found that exporting them directly as SVG did not worked for me that well, so I found on YT another tutorial as on how to export each element as an assest (which can be done in illustatror). tutorial can be foudn here:
     https://www.youtube.com/watch?v=SggOgHs4eyg

For task two implementaiton of poster by using HTML and CSS: i started by created the background layout wich contianed by 7 main SVG elements - the wave in different colors elements. And i used absolute - positioing and viewport units to diplay them in the middle, as well as z-index to some of the can be placed on top or underenath eachother. 



teskt for meg selv -------------
--- Setting margin: 0; on the SVG elements within the .svg-container would remove the auto margin that was previously centering them horizontally. When you set margin: 0;, you do not need to rely on the flexbox properties for centering anymore, as the auto margin was responsible for centering the elements. 

/// #layer__white,
  #layer__blue1,
  #layer__blue--transperant,
  #layer__orange,
  #earth__blue,
  #footer__white, 
  #footer__blue{
    width: 35vw;
    height: auto;
    display: block;
    /*margin: auto;*/
    position: absolute;
    left: 32.5vw;

--- When you use absolute positioning on an element, top, right, bottom, and left properties are used to specify the exact position of the element relative to the nearest positioned ancestor. In this case, setting margin: 0; alone may not have the desired effect because margin does not apply to absolutely positioned elements in the same way as it does with elements in the normal flow. 

When you position an element absolutely, it is taken out of the normal document flow, and margins no longer affect its position relative to other elements. Absolute positioning allows you to specify the exact pixel values for the position of the element using top, right, bottom, and left.

-- the stroke was brought from illustrator but it doesnt do that much: /*
#layer__white,
#layer__blue1,
#layer__blue--transperant,
#layer__orange,
#footer__white,
#footer__blue{
    stroke-width: 0px;
}*/
