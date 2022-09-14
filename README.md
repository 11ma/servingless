# Up and Running with Serverless Functions (Jamstack Explorers)

Learn how to use serverless functions in less than 30 minutes!

📼: [Free Video Course](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/)

## 📚 Resources

| Lesson                                                                                                                                                                                                | Start Branch                                                                                              | End Branch                                                                                            |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| [Introduction with Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/introduction-with-serverless-functions)                                         | -                                                                                                         | -                                                                                                     |
| [Project Setup with Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/project-setup-with-serverless-functions)                                       | [Start Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/02-begin) | [End Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/02-end) |
| [Create Your First Serverless Function](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/create-your-first-serverless-function)                                           | [Start Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/03-begin) | [End Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/03-end) |
| [Integrate with a Third Party API with Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/integrate-with-a-third-party-api-with-serverless-functions) | [Start Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/04-begin) | [End Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/04-end) |
| [Deploying Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/deploying-serverless-functions)                                                         | -                                                                                                         | -                                                                                                     |
| [Customizing the Request with Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/customizing-the-request-with-serverless-functions)                   | [Start Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/06-begin) | [End Code](https://github.com/netlify/explorers-up-and-running-with-serverless-functions/tree/06-end) |
| [The Power of Atomic Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/the-power-of-atomic-serverless-functions)                                     | -                                                                                                         | -                                                                                                     |
| [Next Steps with Serverless Functions](https://explorers.netlify.com/learn/up-and-running-with-serverless-functions/next-steps-with-serverless-functions)                                             | -                                                                                                         | -                                                                                                     |

## notes on serverless

- functions does not work with using Import, returns error below

  `{ "errorMessage":"Unexpected token 'export'", "errorType":"SyntaxError", "level":"error", "stackTrace":[ "ort const handler = async () => {", "^^^", "", "taxError: Unexpected token 'export'", "Object.compileFunction (node:vm:352:18)", "wrapSafe (node:internal/modules/cjs/loader:1031:15)", "Module._compile (node:internal/modules/cjs/loader:1065:27)", "Object.Module._extensions..js (node:internal/modules/cjs/loader:1153:10)", "Module.load (node:internal/modules/cjs/loader:981:32)", "Function.Module._load (node:internal/modules/cjs/loader:822:12)", "Module.require (node:internal/modules/cjs/loader:1005:19)", "require (node:internal/modules/cjs/helpers:94:18)", "Object._executeSync (/usr/local/lib/node_modules/netlify-cli/node_modules/lambda-local/build/lambdalocal.js:277:26)", "/usr/local/lib/node_modules/netlify-cli/node_modules/lambda-local/build/lambdalocal.js:95:26" ] }`

- to use esm with netlify use:

```
[functions]
  node_bundler = "esbuild"
```

[sauce](https://answers.netlify.com/t/lambda-function-es-module-support/30673/14)
