# mauibuttonswithimages
Repro for images in buttons issue in Maui


### Description

Button with an image fails to correctly scale the source image to the size of the button this results in the full size image being displayed in Android and a skewed image in iOS

iOS
![Simulator Screen Shot - iPad Pro (12 9-inch) (5th generation) - 2022-08-29 at 17 43 58](https://user-images.githubusercontent.com/4401594/187150523-b3df1c90-fbf6-48c4-b62a-d4b216d391d7.png)

Android
![Screenshot_1661759181](https://user-images.githubusercontent.com/4401594/187151067-a0fe8632-6356-4a6f-8740-4afc8f0b40f3.png)

WinUI
![Screenshot 2022-08-29 180009](https://user-images.githubusercontent.com/4401594/187153561-5f161def-1d13-48c1-b8e6-a487a0d30cf9.png)



### Steps to Reproduce

Create a new example Maui App

Add the following line of xaml to MainPage.xaml

```
<Button
                ImageSource="dotnet_bot.png"
                Text="Im a happy button"
                HeightRequest="40"
                WidthRequest="200"/>
```

Run the solution, works correctly in WinUI and results in the full sized image next to the button in Android and the image skewed and distorted but with the correct height in iOS 
