# Understanding JWT Tokens

## What is a JWT Token?

JSON Web Token (JWT) is a compact and self-contained way to represent information between two parties. It's often used for authentication and authorization in web applications. A JWT consists of three parts: a header, a payload, and a signature. Let's break down what each part does and how to decode a JWT.

## JWT Structure

A JWT looks like this:

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

It consists of three parts separated by dots:

1. **Header**: Contains information about the type of token and the hashing algorithm used.
   
2. **Payload**: Contains claims (statements about an entity) such as user data, permissions, and other relevant information.
   
3. **Signature**: Ensures the integrity of the token. It's generated using the header, payload, and a secret key.

## Decoding a JWT

Let's take a closer look at each part of a JWT and see how it's decoded:

**1. Header:**

The header is the first part of a JWT, and it typically looks like this when decoded:

```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

- `alg`: Specifies the algorithm used to sign the token (e.g., HS256 for HMAC-SHA256).
- `typ`: Indicates the type of token, which is JWT.

**2. Payload:**

The payload is the second part of a JWT, and it typically contains claims. When decoded, it might look like this:

```json
{
  "sub": "1234567890",
  "name": "John Doe",
  "iat": 1516239022
}
```

- `sub`: Subject of the token (usually a user ID).
- `name`: Name of the user.
- `iat`: Issued At timestamp (when the token was created).

**3. Signature:**

The signature is the last part of a JWT. It's created by taking the encoded header, the encoded payload, and a secret key, and then applying a hashing algorithm. The result is a long string of characters that verifies the token's authenticity.

To decode a JWT, you typically use a JWT library in your programming language of choice. You provide the token and the secret key, and the library will decode and verify the token for you.

## Use Cases

JWTs are commonly used for:

- **Authentication**: Users receive a JWT after logging in, and they send it with each subsequent request to prove their identity.
- **Authorization**: JWTs can contain user roles or permissions, allowing systems to grant or deny access to certain resources.
- **Single Sign-On (SSO)**: A user logs in once and gets a JWT, which can be used to access multiple services without logging in again.

In summary, JWTs are a powerful way to transmit information securely between parties. Understanding how they're structured and decoded is essential for working with authentication and authorization in web applications.