# Edpuzzle-Hack
This code works to speed up your edpuzzle videos that have been locked.


First, select the Ezpuzzle video element from the inspector. (Usually the little arrow icon in the top left of the inspect panel)

![image](https://github.com/sojs-coder/Edpuzzle-Hack/assets/77751154/64dd14a2-270c-4f0f-aef5-62cddfbf6e99)

Once this is done, modify the "id" attribute of the video element to "vid".

### Before:
![image](https://github.com/sojs-coder/Edpuzzle-Hack/assets/77751154/6bb2ef24-bd78-463d-97c9-3cba57b55b9d)

### During:
![image](https://github.com/sojs-coder/Edpuzzle-Hack/assets/77751154/6b102700-e163-4a5b-8263-06e1d7e0787e)

### After:
![image](https://github.com/sojs-coder/Edpuzzle-Hack/assets/77751154/45dadc01-d526-49df-9707-f8f6cafdd75d)

Once this is done, copy and paste the following code into the console:


```js
function changeSpeed(speed=2){
  video = document.getElementById("vid");
  Object.getOwnPropertyDescriptor(HTMLMediaElement.prototype,"playbackRate").set.call(video.speed);
  Object.defineProperty(video, 'playbackRate', {writeable: false});
}
```

Then, you can change the speed by typing `changeSpeed(2)` for 2x, or `changeSpeed(1.5)` for 1.5 times, etc.

