# Why need UWP extention
Universal Windows Platform (UWP). It has delicate UI by using XAML. But it can not support a lot of WIN32 function. That is why we need UWP extention to unlimited it ability. 

# Project describe
Paltform: visual studio 2019  
Function describe: UWP through Windows Desktop Extensions for the UWP tool side loading winform.

# UWP extention
This UWP_extention can side loading winform by using ```FullTrustProcessLauncher.LaunchFullTrustProcessForCurrentAppAsync()```.  

And should generate self-signed certification.  
![image](https://github.com/testtestProblem/UWP_extention/assets/107662393/0aca610e-2e1f-483e-be29-ae0ea8851638)

Add references Windows Desktop Extensions for the UWP in UWP project.  
![image](https://github.com/testtestProblem/UWP_extention/assets/107662393/9c2721f2-0fc4-4a04-8162-bc3da3b69213)

Modify Package.appxmanifest by adding extensions in Windows Application Packaging Project which is showed below.
```
<Extensions>
  <uap:Extension Category="windows.appService">
       <uap:AppService Name="SampleInteropService" />
  </uap:Extension>
	<desktop:Extension Category="windows.fullTrustProcess" Executable="WindowsFormsApp1\WindowsFormsApp1.exe" />
</Extensions>
```


