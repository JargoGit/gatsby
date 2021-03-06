---
title: Deploying to Surge
---

In this guide, you will learn how to deploy your Gatsby site to Surge.

[Surge](https://surge.sh/) is a cloud platform for hosting static websites, which is extremely simple to use but offers customization options for those who need them.

Their generous free tier permits unlimited publishing, using custom domains, basic SSL, with more features available in through the professional plan.

This guide will show you how to get started in a few quick steps:

## Step 1: Getting Started with Gatsby

If you don't already [have a Gatsby project](/docs/quick-start), start by installing Gatsby:

```shell
npm install -g gatsby-cli
```

Then, generate a project with the following:

```shell
gatsby new <project name>
```

## Step 2: Getting Surge

To install the surge CLI with `npm`, paste the following into your terminal:

```shell
npm install -g surge
```

## Step 3: Preparing to Deploy

Build a site by running this command in your project's root directory:

```shell
gatsby build
```

This generates a publishable version of your site in the `./public` folder.

## Step 4: Deploying

You can deploy your site by running the following in the root of the project directory.

```shell
surge build/
```

If this is your first time using surge, you'll be prompted to create a (free) account from the command line. This will only happen once.

Press `enter` to confirm that the path to your `build/` folder is correct, and that you'd like to keep the randomly generated subdomain name (it can be edited if not).

You're done! Your terminal will output the address of the domain where your site was deployed.

## Step 5: Bonus - Remembering a Domain

To ensure future deploys are sent to the same location, you can store the domain name in a [`CNAME`](https://surge.sh/help/remembering-a-domain) file from your project root. Assuming your site was deployed to `https://my-cool-domain.surge.sh`, run the following command:

```shell
echo my-cool-domain.surge.sh > CNAME
```

Consult the [Surge Docs](https://surge.sh/help/) for information about how to customize your deployment further. Remember that each time you redeploy your site, you will need to rerun `gatsby build` first.

## References:

- [Surge Documentation](https://surge.sh/help/)
- [Deploying to a Custom Domain](https://surge.sh/help/adding-a-custom-domain)
