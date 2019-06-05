.. _topics-AndroidManifest配置

================
AndroidManifest配置
================


权限配置
=========================

- 配置网络访问权限

.. code-block:: c

	<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
	<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
	<uses-permission android:name="android.permission.CHANGE_WIFI_STATE" />
	<uses-permission android:name="android.permission.INTERNET"/>


Application 配置
=========================

- 注意：如果targetSdkVersion 28，则需要增加此配置，否则可以忽略AndroidManifest配置

- 在application 增加 android:networkSecurityConfig="@xml/network_security_config"

.. code-block:: c

   <application 
	xmlns:tools="http://schemas.android.com/tools"
	android:allowBackup="false"
	android:icon="@mipmap/ic_launcher"
	android:label="@string/app_name"
	android:supportsRtl="true"
	android:theme="@style/AppTheme"
	tools:replace="android:allowBackup"
	android:usesCleartextTraffic="true"
	android:networkSecurityConfig="@xml/network_security_config">
    </application>


