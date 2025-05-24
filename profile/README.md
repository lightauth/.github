# Light Auth

<p align="center">
    <img src="../images/light-auth.svg" alt="Light Auth Logo" width="120"/>
</p>

[Light Auth](https://lightauth.github.io) is a lightweight authentication solution designed for simplicity and ease of integration.

It provides essential authentication features with minimal configuration, making it ideal for small projects, prototypes, or applications that require straightforward user sign-in functionality.

## Features

- Simple setup and configuration
- Supports basic authentication flows
- Minimal dependencies
- Easily extensible for custom requirements
- Server side an Client side components

## Framework Compatibility

Light Auth shines across your favorite frameworks! Whether you’re building with  

| Icon & Name                                   | NPM Package                                                                 | GitHub Sample                                                                                 |
|-----------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| ![NextJS](../images/nextjs.svg) **Next.js**   | [light-auth-nextjs](https://www.npmjs.com/package/@light-auth/nextjs)       | [Next.js Sample](https://github.com/lightauth/light-auth-nextjs-sample-one)           |
| ![Astro](../images/astro.svg) **Astro**       | [light-auth-astro](https://www.npmjs.com/package/@light-auth/astro)         | [Astro Sample](https://github.com/lightauth/light-auth-astro-sample-one)              |
| ![Nuxt](../images/nuxtjs.svg) **Nuxt**        | [light-auth-nuxt](https://www.npmjs.com/package/@light-auth/nuxt)           | [Nuxt Sample](https://github.com/lightauth/light-auth-nuxt-sample-one)                |
| ![SvelteKit](../images/sveltekit.svg) **SvelteKit** | [light-auth-sveltekit](https://www.npmjs.com/package/@light-auth/sveltekit) | [SvelteKit Sample](https://github.com/lightauth/light-auth-sveltekit-sample-one)      |
| ![Express](../images/express.svg) **Express** | [light-auth-express](https://www.npmjs.com/package/@light-auth/express)     | [Express Sample](https://github.com/lightauth/light-auth-express-sample-one)          |

![LightAuth](../images/light-auth.svg) **Light Auth** integrates seamlessly, letting you add authentication with a sparkle ✨ to any stack!

## Getting Started

> This getting started is based on the  [light-auth-nextjs](https://www.npmjs.com/package/@light-auth/nextjs) package.
>
> You will find examples for all others frameworks in each relevant repository

### Install Light Auth**  

``` sh
npm -i @light-auth/nextjs
```

Follow the installation instructions in the project documentation.

``` ts
import { Google, Github } from "arctic";
import { CreateLightAuth } from "@light-auth/nextjs";

const googleProvider = {
  providerName: "google",
  arctic: new Google(
    process.env.GOOGLE_CLIENT_ID,
    process.env.GOOGLE_CLIENT_SECRET,
    "http://localhost:3000/api/auth/callback/google"
  ),
};


const githubProvider = {
  providerName: "github",
  arctic: new GitHub(
    process.env.GITHUB_CLIENT_ID,
    process.env.GITHUB_CLIENT_SECRET,
    "http://localhost:3000/api/auth/callback/github"
  ),
};

export const { providers, handlers, signIn, signOut, getSession, getUser } = CreateLightAuth({
  providers: [googleProvider, githubProvider]
```

2. **Configure Authentication**  
    Set up your authentication settings as described in the configuration guide.

3. **Integrate with Your App**  
    Import and use Light Auth in your application code.

## Documentation

See the [docs](../docs) directory for detailed usage instructions, API reference, and examples.

## Contributing

Contributions are welcome! Please open issues or submit pull requests to help improve Light Auth.

## License

This project is licensed under the MIT License.
