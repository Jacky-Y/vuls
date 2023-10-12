## zzzcms-V2.2.0 has an arbitrary URL redirection vulnerability.
The official website for this CMS is http://www.zzzcms.com/a/news/31_313.html

You can download the CMS from http://115.29.55.18/zzzphp.zip

## 1. Download and install zzzcms. After installation is complete, go to the homepage.
![image-url1](images/url1.png)

## 2. Click on the registration button in the top right corner and register a new user.
![image-url2](images/url2.png)
![image-url3](images/url3.png)

## 3. Navigate to the personal profile page in the user center. In the text box for personal introduction, enter the payload: <meta http-equiv=refresh content=2,url=http://www.baidu.com> and save.
![image-url4](images/url4.png)

## 4. Now go to the account information page in the user center. This page will automatically redirect to the website http://www.baidu.com.
![image-url5](images/url5.png)
![image-url6](images/url6.png)

## 5. When you view the source code, the payload has been inserted into the html page.
![image-url7](images/url7.png)


