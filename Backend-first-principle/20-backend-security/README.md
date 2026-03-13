##

## Lots of research
What could go wrong here?
1. Injection attacks
    '' OR '1'='1' --'
    ```SQL
        -- SELECT * FROM users WHERE email = "'' + [user input] + "'";
        
        SELECT * FROM users WHERE email = 'alice@gmail.com'

        -- SELECT * FROM users WHERE email = '' OR '1'='1' --';

        -- SELECT * FROM users WHERE true;

        -- SELECT * FROM users;

        SELECT * FROM users WHERE email = ''; DROP TABLE users --'
    ```

    ```js
        const stmt = 'SELECT * FROM users WHERE email = $1';
        DBQuery(stmt, input);
    ```
    2. Command Injection

    3. Authentication
      - stateful suthentication
      db
      redis
      cache
      - social authentication
      Oauth flow
      - password storage
      Lucia
      hashing
      hashing + salting

    coockies:
      HttpOnly -- XSS Vulnarability prone
      secure: true over https, not http
      samesite
        strict
        lax
        none

    JWT and serverless authentication
     - server does not need to store everything in db
     - Revocation is hard --> if users account is compromised
       - blacklisted token
       - short expiration refresh token
          - access token - very short ~5m
          - refresh token - 1d. 7d on expire 401 error
          (not perfect work arround)
    where is the ideal spot to store jwt token.
     - local storage( not a good choice, since xss can steal it)
     - cookie (HTTPOnly)
     
     unless have specific scaling requirements like horizontal scaling, multiple servers being able to authenticate a particular user request - always prefer stateful authentication/ session based authentication over stateless authentication

     revocation strategies are straight forward and the whole work

     ### Rate limiting

     have multiple layers 
      - per IP
        botnets
        proxy
      - per account 
      - global rate limiter

      ### Authorization issue
      
        


