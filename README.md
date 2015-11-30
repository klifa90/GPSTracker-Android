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