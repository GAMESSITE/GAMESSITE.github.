  <!DOCTYPE html>
<html>
<head>
<meta charset=utf-8 />


  <link href="https://unpkg.com/video.js/dist/video-js.css" rel="stylesheet">
</head>
<body>


  <video-js id="my_video_1" class="vjs-default-skin" controls preload="auto" width="640" height="268">
    <source src="http://example.com/iptv.mru8" type="application/x-mpegURL">
  </video-js>

  <script src="https://unpkg.com/video.js/dist/video.js"></script>
  <script src="https://unpkg.com/@videojs/http-streaming/dist/videojs-http-streaming.js"></script>

  <script>
    var player = videojs('my_video_1');
  </script>
 <script>
document.getElementById('file').onchange = function(){

  var file = this.files[0];

  var reader = new FileReader();
  reader.onload = function(progressEvent){
    // Entire file
    console.log(this.result);

    // By lines
    var lines = this.result.split('\n');
    for(var line = 0; line < lines.length; line++){
      console.log(lines[line]);
    }
  };
  reader.readAsText(file);
}; 

  var mySubString = str.line(
    str.lastIndexOf("#EXTINF:-1,") + 1, 
    str.lastIndexOf("http:/")
);
</script>
<input type="file" name="file" id="file">


</body>
</html>
