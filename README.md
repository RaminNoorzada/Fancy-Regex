const regex = /[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}/;
const email = "example@example.com";

if (regex.test(email)) {
    console.log("Valid email address");
} else {
    console.log("Invalid email address");
}
In the example above, we define a regular expression pattern using the RegExp constructor and store it in the regex variable. We then define an email variable containing the email address we want to validate.

We use the test method of the RegExp object to match the regular expression pattern against the email variable. The test method returns true if the email address matches the regular expression pattern and false otherwise.

We then use an if statement to check if the email address is valid or not and log the appropriate message to the console.

Note: Regular expressions in JavaScript are also enclosed in forward slashes /.../.