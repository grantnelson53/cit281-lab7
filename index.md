## Lab 7

In this lab, we learned all about error handling and debugging 

### Source Code 

    class CustomError extends Error {

        constructor() { }

        throwGenericError() {
            throw new Error("Error: Generic error");
        }

        throwCustomError() {
            throw new CustomError("Error: Custom error")
        }


    }

    console.log("Force Generic Error");
    try {
            // Code that may have a problem

            console.log("Generic Error try block");
            myErrObj.throwGenericError();

    }
    catch {
            // If an error occurs in the try block
            console.log("Generic Error catch block");
            myErrObj = new Error();
            console.log("Error: generic error");

    }
    finally {
            // No matter what, regardless if the code broke or not, run this code 
            console.log("Generic Error finally block");
    }


    console.log("Force Custom Error");
    try {
      // Code that may have a problem

      console.log("Custom Error try block");
      myErrObj.throwCustomError();
    } catch {
      // If an error occurs in the try block
      console.log("Custom Error catch block");
      myErrObj = new Error();
      console.log("CustomError: custom error");
    } finally {
      // No matter what, regardless if the code broke or not, run this code
      console.log("Custom Error finally block");
    }
