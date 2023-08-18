**1. Install the plugin "WP Event Manager – Events Calendar, Registrations, Sell Tickets with WooCommerce" from the plugin marketplace. After that, activate the plugin.**
![image-wpxss1](images/wpxss1.png)

**2. Navigate to the URL: http://word.test/wp-admin/edit.php?post_type=event_listing&page=event-manager-form-editor.**
![image-wpxss2](images/wpxss2.png)

**3. Launch Burp Suite to capture the network traffic.**
![image-wpxss2](images/wpxss3.png)

**4. Click on "save changes" below the form. Burp Suite will intercept the outgoing POST request.**
![image-wpxss4](images/wpxss4.png)
![image-wpxss5](images/wpxss5.png)

**5. Modify the value of the event[event_title][type] parameter to oNmOuSeOvEr=prompt(1)//, and then allow the request to proceed.**
![image-wpxss6](images/wpxss6.png)

**6. After moving the cursor over the table, a popup will appear on the web page. Logging out and logging back in still triggers the XSS.**
![image-wpxss7](images/wpxss7.png)

**7. Switch to the "tom" user account (which also has admin privileges), and moving the cursor over the table again will trigger the XSS. This behavior suggests that it might be a stored XSS.**
![image-wpxss88](images/wpxss88.png)

**8. However, it's not just the event[event_banner][type] parameter that can cause XSS. In fact, it is the event[xxx][type] parameter located in the first row of this form that causes XSS. By dragging the button on the left of each row and moving it to the first row, then modifying the POST request's event[xxx][type] to oNmOuSeOvEr=prompt(1)//, XSS can also be triggered. For instance, if you move the "Event Banner" row to the top and modify the POST request's event[event_banner][type] to oNmOuSeOvEr=prompt(1)//, a popup will appear when the cursor is moved over the form.**
![image-wpxss9](images/wpxss9.png)
![image-wpxss10](images/wpxss10.png)
