<!DOCTYPE html>
<html>
<head>
  <title>Upload Photo</title>
  <script src="https://upload-widget.cloudinary.com/global/all.js" type="text/javascript"></script>
</head>
<body>
  <button id="upload_widget">Upload Photo</button>
  <p id="result"></p>

  <script type="text/javascript">
    var myWidget = cloudinary.createUploadWidget({
      cloudName: 'dm7gfgtgq',
      uploadPreset: 'MIRROR FOR SOUL'
    }, (error, result) => {
      if (!error && result && result.event === "success") {
        document.getElementById("result").innerText = result.info.secure_url;
      }
    });

    document.getElementById("upload_widget").addEventListener("click", function(){
      myWidget.open();
    }, false);
  </script>
</body>
</html>
