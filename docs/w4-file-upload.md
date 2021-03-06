# It's 90's again
1. Make an empty HTML page (or use [HTML5 Boilerplate](https://html5boilerplate.com))
2. Make a form which uploads a file to the [Media API](https://github.com/mattpe/wbma/blob/master/docs/w3-media-api.md)
  * Form should have these fields:
    * file
    * user
    * title
    * description
    * type (values: image/video/audio)
    * mime-type (example values: image/jpg, video/mp4, audio/mp3)
3. Study the request parameters in Developer Tools / Network

# Back to the future
1. [Setup AngularJS Environment like in first lab](https://github.com/mattpe/wbma/blob/master/docs/w1-toolchain.md#exercise-1-setup-your-toolchain-and-a-new-web-project)
  * seed project: https://github.com/mattpe/wbma-seed can be used as template
2. Use AngulrJS's $http.post shortcut method to upload the file
  * Example:
  ```
  $scope.fd = new FormData(SELECT FORM ELEMENT WITH JAVASCRIPT);
  $scope.sendImage = function(){
    var request = $http.post('http://util.mw.metropolia.fi/ImageRekt/api/v2/upload', $scope.fd, {
        transformRequest: angular.identity,
        headers: {
            'Content-Type': undefined
        }
    });
    request.then(.......);
  }
  ```
  * [FormData API](https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using_FormData_Objects)
  * [Teacher's example](https://github.com/ilkkamtk/w4-ex1)
