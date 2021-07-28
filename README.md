# gatsby-source-directus

> The unofficial Gatsby source plugin for Directus CMS projects

Build by [gatsby-graphql-toolkit](https://github.com/syfxlin/gatsby-graphql-toolkit)

## Configuration

```js
// gatsby-config.js
module.exports = {
  plugins: [
    {
      resolve: "gatsby-source-directus",
      options: {
        url: process.env.DIRECTUS_URL,
        token: process.env.DIRECTUS_TOKEN,
      },
    },
    {
      resolve: "gatsby-source-graphql",
      options: {
        typeName: "Directus_System",
        fieldName: "directusSystem",
        url: `${process.env.DIRECTUS_URL}/graphql/system`,
        headers: {
          Authorization: `Bearer ${process.env.DIRECTUS_TOKEN}`,
        },
      },
    },
  ],
};
```
