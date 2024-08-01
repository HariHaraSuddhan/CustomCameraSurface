

-------------------------------------------------Ionic Info--------------------------------------------------------------------------

Ionic:

   Ionic CLI                     : 7.1.1 (C:\Users\hari.s\AppData\Roaming\nvm\v19.9.0\node_modules\@ionic\cli)
   Ionic Framework               : @ionic/angular 8.2.6
   @angular-devkit/build-angular : 18.1.3
   @angular-devkit/schematics    : 18.1.3
   @angular/cli                  : 18.1.3
   @ionic/angular-toolkit        : 11.0.1

Capacitor:

   Capacitor CLI      : 6.1.1
   @capacitor/android : 6.1.1
   @capacitor/core    : 6.1.1
   @capacitor/ios     : not installed

Utility:

   cordova-res : not installed globally
   native-run  : 2.0.1

System:

   NodeJS : v19.9.0 (C:\Program Files\nodejs\node.exe)
   npm    : 9.6.3
   OS     : Windows 10

Required Java Version is 17
--------------------------------------------------------------------------------------------------------------------------------------

    <!-- Permissions --> give this permission in AndroidManifest.xml

    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.CAMERA" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />

----------------------------------------------------------------------------------------------------------------------------------------

	Add this line in MainActivity,java

package io.ionic.starter;

import android.os.Bundle;
import com.getcapacitor.BridgeActivity;
import com.getcapacitor.Plugin;
import com.ahm.capacitor.camera.preview.CameraPreview;
import java.util.ArrayList;

public class MainActivity extends BridgeActivity {
    @Override
    public void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);
        registerPlugin(CameraPreview.class);
    }
}

-----------------------------------------------------------------------------------------------------------------------------------------

Required Plugin to install

npm i '@capacitor-community/camera-preview'