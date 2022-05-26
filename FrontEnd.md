# CREATING FOUR VIDEO STREAM VIEWER FOR THE AMAZON WEB SERVIVCES CAMERA USING BOOTSTRAP

- The purpose for creating 4 video streams viewer is to enable us to be able to view 4 different cameras on the same screen at the same time.

## TAGS AND CLASSES USED WHEN CREATING FOUR VIDEO STREAM VIEWERS IN BOOTSTRAP

- The ```<div> (Division)``` tag defines a division or a section in an HTML document.
- Class-Containers are the most basic layout element in Bootstrap and are required when using the default grid system.
- Class-row is a wrapper for columns.
- Class-Colunm- creates gutters (gaps between column content) via padding.
- Paddling (p)- clears the space around the content(video streams).

# PROCEDURE TO FOLLOW WHEN CREATING FOUR VIDEO STREAM VIEWER
 
 - In order to have the first two Video Stream Viewer on the front-end the following steps 1-3 can be done twice.

- Step 1

      - Create a Div and a class named ```main``` e.g : ```<div class ="main></div>```.

- Step 2

       - Then write a class named row inside the div and class named main e.g: <div class ="main"><div class="row"></div></div>

- Step 3 

    -   After writing the class named row, you can write the div and class named column(col) with paddling of 3, e.g
        
      <div class ="main>
           <div class="row"> 
               <div class="col p-3"></div>
            </div>
           </div> 
**Note**     
  -   In order to have four video stream viwer on the front-end step 4 and five should be reaped.

  - Step 4

       - Then write a class named column(col) md-6 (medium of 6) inside the div and class named row e.g: 
       <div class ="main>
           <div class="row"> 
               <div class="col p-3"></div>
            </div>
             <div class ="row> 
               <div class="col-md-6">
                  </div>
            </div>
           </div> 

- Step 5

      - After writing the class named row and column(col-md-6) you can write the div and an id named playerContainer, e.g:
       
       <div class ="main>
           <div class="row"> 
               <div class="col p-3"></div>
            </div>
              <div class ="row>
           <div class="col-md-6"> 
               <div id="playerContainer"></div>
            </div>
           </div>
           </div>
    - Step 6
        - Here is the summary of how it should look like.
       write: 

                
                 <div class ="main>
                 <div class="row"> 
                   <div class="col p-3"><div id="playerContainer"></div></div>
                   <div class="col p-3"><div id="playerContainer"></div></div>
            </div>
                 <div class ="row> 
                    <div class="col-md-6">
                      <div id="playerContainer></div>
                    </div>
                    <div class="col-md-6">
                     <div id="playerContainer"></div>
            </div>
           </div> 
        
                                                                                

