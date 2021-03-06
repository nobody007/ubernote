Example code for my blog post http://out-println.appspot.com/posts/offline_example.

## Browser support

* Firefox: all tests pass. However, I've sometimes observed erratic behavior when testing manually: the offline cache stops updating, I have to clear it and restart the browser;
* Chrome: all tests pass, but I get random errors in the Selenium tests (where DOM elements seem to be uninitialized) ;
* Safari: same as Chrome, but the errors happen much more often.

## Running

Install the Play! framework as explained [here](http://www.playframework.org/documentation/1.2.1/guide1#aInstallingthePlayframeworka).

To run the application, type `play run --%prod` in the application's root directory.

To run the unit tests, type `play test`, navigate to http://localhost:9000/@test and click the 'Run all' link.


## Reading the code

If you're new to Play!, this should get you started:

* `conf/routes` maps URIs to controller methods (controllers are in `app/controllers`);
* when a controller calls `render()`, the corresponding template in `app/views` is invoked.

For more information, refer to [the Play! documentation](http://www.playframework.org/documentation/1.2.1/home).
