# GetSetPropeties
                                                                           Code
																	-------------------
GetProperty
------------

		Proc = Runtime.getRuntime().exec("/system/bin/getprop gsm.version.ril-impl");

		 InputStream stdin = Proc.getInputStream();
		 InputStreamReader isr = new InputStreamReader(stdin);
		 BufferedReader br = new BufferedReader(isr);
		 String line = null;
		 Log.d("Shell" ,"<OUTPUT>");
		 while ( (line = br.readLine()) != null)
			 Log.d("Shell" , line);
		 Log.d("Shell", "</OUTPUT>");
		 int exitVal = Proc.waitFor();
		 Log.d("Shell","Process exitValue: " + exitVal);
SetProp
------------

		Proc =Runtime.getRuntime().exec("/system/bin/setprop service.Mypropety Value");

		 InputStream stdin = Proc.getInputStream();
		 InputStreamReader isr = new InputStreamReader(stdin);
		 BufferedReader br = new BufferedReader(isr);
		 String line = null;
		 Log.d("Shell" ,"<OUTPUT>");
		 while ( (line = br.readLine()) != null)
			 Log.d("Shell" , line);
		 Log.d("Shell", "</OUTPUT>");
		 int exitVal = Proc.waitFor();
		 Log.d("Shell","Process exitValue: " + exitVal);
Manifest
-----------
		<?xml version="1.0" encoding="utf-8"?>
		<manifest xmlns:android="http://schemas.android.com/apk/res/android"
			package="com.User.vibrationmeter"
			android:sharedUserId="android.uid.system">

			<application
				android:allowBackup="true"
				android:icon="@mipmap/ic_launcher"
				android:label="@string/app_name"
				android:supportsRtl="true"
				android:theme="@style/AppTheme">
				<activity
					android:name=".MainActivity"
					android:screenOrientation="portrait"
					android:label="@string/app_name"
					android:theme="@style/AppTheme.NoActionBar">
					<intent-filter>
						<action android:name="android.intent.action.MAIN" />
						<category android:name="android.intent.category.LAUNCHER" />
					</intent-filter>
				</activity>
			</application>

		</manifest> 
