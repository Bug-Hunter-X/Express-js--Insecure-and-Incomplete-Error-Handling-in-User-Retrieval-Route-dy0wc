# Express.js Insecure Error Handling
This repository demonstrates a common error in Express.js applications: inadequate error handling in API routes.  The example shows a route that retrieves user data by ID.  However, it lacks proper checks for invalid input and database errors.

**Vulnerability:** The code doesn't handle cases where `req.params.id` is not a valid number or when the user is not found in the database. This can lead to unexpected behavior or crashes.  Further, the generic `User not found` message doesn't provide helpful debugging information or prevent potential vulnerabilities.

**Solution:** The `bugSolution.js` file demonstrates improved error handling practices.