	
	Ionic framework starter:

		Small prototype created to test the framework and have an opinion about it

	Prerequisites:

		- Node/Npm
		- Sass
		- Angularjs

			* http://ionicframework.com/docs/overview/
			Ionic currently requires AngularJS in order to work at its full potential. While you can still use the CSS portion of the framework, you'll miss out on powerful UI interactions, gestures, animations, and other things. In the future we'd like to expand beyond Angular to support other frameworks.
			
			https://github.com/driftyco/ionic/issues/325

			* Angular 2 is getting released soon (and there's a lot of changes), Ionic is offering support: http://blog.ionic.io/angular-2-ionic/

		- Gulp (optional)


	Dependencies:

		- cordova
		- ionic

			* npm install -g cordova ionic (installed globally)


	Start guide:
	
		- generate:

			app:

				ionic start [PROJECT NAME]	

				* generates with default template

			template (clone):

				ionic start [PROJECT NAME] [TEMPLATE NAME]

				* to get the templates run `ionic templates`


			What we are doing is cloning and modifying the initial project structure that can be from the blank template, tabs or maps template, etc onto an actual customised app. Remember we're building an hybrid app.


		- Build & Emulate:

			xcode (dependency for ios):

				ionic build ios
				ionic emulate ios *1
				ionic serve

			android

				ionic build android
				ionic emulate android *1
				ionic serve

			* `serve` uses livereload

			* Other commands:

				display both Android and iOS side by side:

					ionic serve --lab

				*1 ionic platform add [PLATFORM], example
				*1 ionic platform add android

		- Creating new project:

			- install dependencies running npm install

	
	Emulator:

		For android:

			- Install the Android SDK
			- Add the Android SDK Path to the the OS Environment Path
			- Since the default Android AVD (Android Virtual Device) is really slow, use Genymotion instead (also slow, but better). It's possible to test on the device, but unfortunately at the time of writting, the device wasn't detected `adb devices -l`

			* this steps don't work on windows Bash emulator for some reason, so all the comands should run on `powershell` if windows

			* fixing issue (if device not detected `adb  devices`):

				https://androidsecurity.wordpress.com/2013/06/05/install-google-nexus-4-adb-usb-drivers-on-windows-android-studio/


				Samsung USB drivers
				
					http://developer.samsung.com/technical-doc/view.do?v=T000000117


				Google USB Driver:

					http://developer.android.com/sdk/win-usb.html

				OEM usb:

					http://developer.android.com/tools/extras/oem-usb.html#InstallingDriver


				Restart adb server:

					adb kill-server
					adb start-server
					adb devices

				Other fix:

					Ensure debugging is enabled
					Install device drivers
					If it still doesn't work use this http://koush.com/post/universal-adb-driver, reboot and try again should definitely work.


	Resources:


		learn ionic:

			http://learn.ionicframework.com/

		Cordova api / extensions:

			http://ngcordova.com/

		Ionic Framework Demo by Matt Stauffer:

			https://www.youtube.com/watch?v=nh9EARpk-dc


		Geny motion:

			https://www.genymotion.com