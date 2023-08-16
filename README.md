Steps-

1. Import necessary libraries:
   - `smtplib`: This library provides an interface to send emails using the Simple Mail Transfer Protocol (SMTP).
   - `email.mime.text`: This module allows you to create and format plain text email content.
   - `email.mime.multipart`: This module enables you to create multipart email messages (with both plain text and HTML parts).

2. Email Configuration:
   - Set the sender's email address (`sender_email`) and password (`sender_password`) to authenticate with the SMTP server.
   - Specify the recipient's email address (`receiver_email`), subject of the email (`subject`), and the body of the email (`body`).

3. Create MIME Object:
   - Create a `MIMEMultipart` object named `message`.
   - Set the sender, recipient, and subject in the `message` object.
   - Attach the plain text body to the `message` object using `MIMEText`.

4. Connect to SMTP Server:
   - Specify the SMTP server (`smtp_server`) and port (`smtp_port`). In this case, the example uses Gmail's SMTP server and port 587 for TLS encryption.
   - Create an SMTP server instance using `smtplib.SMTP`.
   - Initiate a secure connection using `starttls()`.

5. Log In to Email Account:
   - Log in to the sender's email account using `server.login()` with the sender's email and password.

6. Send the Email:
   - Convert the `message` object to a string format using `.as_string()`.
   - Use `server.sendmail()` to send the email. Provide the sender's email, recipient's email, and the email content.

7. Quit the Server:
   - Close the connection to the SMTP server using `server.quit()`.

8. Print Success:
   - Print a success message indicating that the email has been sent.

Note:
- The example uses Gmail's SMTP server for demonstration purposes. Depending on the email provider you use, you may need to modify the SMTP server and port settings.
- The provided code does not include extensive error handling. In a production environment, you would want to handle exceptions and errors more gracefully.
- To use this code, replace placeholders like `YOUR_EMAIL`, `YOUR_PASSWORD`, `TO_EMAIL`, and the email content with actual values.

Remember to use this code responsibly and avoid sharing sensitive information, such as your email credentials, in your code or publicly.
