# Stem Day 2016

## Files
To see each web page simply double click the file and it will open in your default browser.
+ **stem_initial.html:** This is the empty template we started with in class. If you open it, it is just an blank web page.
+ **stem.html:** This is the web page we completed in class. 

*Feel free to experiment! If something doesn't work you can always download the files again and start from scratch*


## Body
We first added some content to the page in between the `<body>` and `</body>` tags.
#### Text 
We added some simple text with the h1 tag. `<h1>STEM DAY 2016</h1>`
#### Image
We added a picture with the img tag. `<img src="starwars.jpg"/>`
#### Button
We added a button. We put it in between div tags to make sure it positioned under the image.
```
  <div>
      <button>Use the force!</button> 
  </div> 
```


## Style
We wanted to add some style to our page.  We put css between the `<style>` and `</style>` tags.
#### Color
We changed the color of our text using an h1 selector and the color propery.
```
  h1{
     color: green; 
  } 
```
#### Font Size
We wanted the button to be bigger so we increased the size of the text with a button selector and font-size property.
```
  button {
      font-size: 30px;
  } 
```

## Code
Finally, we added some javascript *code* in between the `<script>` and `</script>` tags. We didn't spend a lot of time on the details. This code was prepared ahead of time to "wire up" our button so that when we click it, it would *rotate* the image and set a *transition*.
```
  window.onload = function() {
      var button = document.querySelector('button');
      button.addEventListener("click", useTheForce);
  }
  
  function useTheForce() {
      var starWarsImage = document.querySelector('img');
      starWarsImage.style.transition = null;
      starWarsImage.style.transform = null;
      setTimeout(function() {
          starWarsImage.style.transition = "transform 10s";
          starWarsImage.style.transform = "rotate(3600deg)";     
      }, 10);
  }
```
The following two lines can be modified to *experiment* wih the web page. The **10s** represents "10 seconds". Change it values like 1s or 30s to see the difference in how long it takes to rotat the image. The **rotate(3600deg)** spins the image 3600 degrees like propellor.  Set the 3600deg to 90deg or even 10000deg to see it rotate more or less times.
```
  starWarsImage.style.transition = "transform 10s";
  starWarsImage.style.transform = "rotate(3600deg)"; 
```

