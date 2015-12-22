Android Singleton GPSTracker
=====================

Simple class for initializing location services, start and stop obtaining coordinates. Works with GPS and/or network location.
It includes an alert dialog to show when location is disable

It can be used as a singleton class or as a service

Include permissions
  
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />    
    <uses-permission android:name="android.permission.INTERNET" />
 
## Custom Criteria
 
For a custom criteria, define:

	final Criteria criteria = new Criteria();
	criteria.setAccuracy(Criteria.ACCURACY_FINE);
	criteria.setSpeedRequired(true);
	criteria.setAltitudeRequired(false);
	criteria.setBearingRequired(false);
	criteria.setCostAllowed(true);

	final String bestProvider = locationManager.getBestProvider(criteria, true);

	locationManager.requestLocationUpdates(bestProvider, 1, 0.0f, this);
	
## License

    The MIT License (MIT)

    Copyright (c) 2015 Klifa(http://www.spacedevuy.com)

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.