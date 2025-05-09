# LXDAO Developer Guide

This document introduces the tech stacks, branch styles, development workflow, and code styles in LXDAO. The topic on forum is: <https://forum.lxdao.io/t/lxdao-develop-guide-is-out/94>.

## Tech stacks

Try to use as simple as possible tech stacks to finish the project, DO NOT introduce unnecessary tools, libraries, etc.

### Languages

- JavaScript / TypeScript for full stack developments
- Python for crawlers or scripts
- Solidity for smart contracts
- Others for specific projects

### FrontEnd

- React.js Ecosystem
- [Next.js](https://nextjs.org/)
- [MUI](https://mui.com/) for UI components
- [RainbowKit](https://www.rainbowkit.com/) for connecting wallet
- [Wagmi](https://wagmi.sh/) for Ethereum hooks

### BackEnd

- Nest.js for APIs
- Redis for cache
- PostgreSQL + [Prisma](https://www.prisma.io/) for ORM
- Nest.js swagger for APIs test
- [Thegraph](https://thegraph.com/) for blockchain data

### SaaS and Cloud Services

- [Vercel](https://vercel.com/) for FrontEnd projects and simple FaaS logic requirements
- [Heroku](https://www.heroku.com/) for simple BackEnd APIs
- AWS AKS for complex BackEnd applications
- AWS Lightsail for DEV environment

### Others

- Prettier for code format
- ESLint for code linting
- GitHub Actions for CICD
- VSCode
- [Writing guidelines](https://github.com/sparanoid/chinese-copywriting-guidelines)
- [DappReader](https://DappReader.com) Debugging Smart Contracts as easy as using the Postman

## Development

### Environment

- `Local` your local machine
- `DEV` remote testing and preview environment
- `SIT` only for big projects, for on-production verification
- `Production` production environment for users

`Local`, `DEV`, and `Production` are required environments, `SIT` just for big projects.

### Branch styles

- `main` for `Production` environment, the code in this branch reflects the latest production application, protected by default
- `develop` for `DEV` or `SIT` environment, latest version of code
- `feature/[feature-name]` for specific changes
- `fix/[defect-name]` for bugfix

### Development workflow

- Create or get a ticket on the Project Management tool ([ClickUp](https://clickup.com/))
- Checkout a branch from `develop` for the change, the branch name should follow the pattern: `feature/[feature-name]`, `fix/[defect-name]`
- Coding on your local machine
- Submit a PR to the `develop` branch, verify and test on the `DEV` environment
- Submit a PR from `develop` to `main`, ask someone to do code review and approve your PR
- After merging into `main`, will deploy your code to production

### Code Styles

We follow loose version of [Airbnb JavaScript Style Guide](https://airbnb.io/javascript/react/). Pretty much the default config from [Prettier](https://prettier.io/). Please install the Prettier plugin and create the following configuration in your project:

```
{
  "singleQuote": true,
  "trailingComma": "all"
}
```

TODO add more details

### Commit Message Styles

We follow loose version of [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). In short:

- `feat:` for features and most of the changes
- `chore:` for trivial changes, like code formatting
- `fix:` for bugfixes
- `docs:` for updating documents

## Add LXDAO information in README.md, Website, etc.

As a part of LXDAO, the project buidl in LXDAO or buidl with LXDAO should show some information about LXDAO.

For example, add the following information at the bottom of the README.md file.

```
## Supported by LXDAO

<a target="_blank" href="https://lxdao.io/"><img alt="Supported by LXDAO" src="https://bafkreib7wsfivsbtinvx7yfou2b556ab32pojbjutkxfhh7v3y45qkevui.ipfs.nftstorage.link/" width="180" /></a>

This is a project supported by LXDAO. More links: [LXDAO](https://lxdao.io/) | [LXDAO Forum](https://forum.lxdao.io/) | [LXDAO Discord](https://discord.lxdao.io) | [LXDAO Twitter](https://twitter.com/LXDAO_Official).

LXDAO is an R&D-focused DAO in Web3. Our mission is: Gather the power of buidlers to buidl and support “LX” (valuable) Web3 projects sustainably and welcome 1 billion users into Web3. Welcome to join us.

[![Join our Discord server!](https://invidget.switchblade.xyz/HtcDdPgJ7D)](http://discord.gg/HtcDdPgJ7D)
```

## Music when coding 😁

- [The Midnight](https://www.youtube.com/channel/UC-sM_PLqzgktdUcW2LEKKkQ)

## References

- [How to contribute React](https://reactjs.org/docs/how-to-contribute.html)
- [Airbnb JavaScript Style Guide](https://airbnb.io/javascript/react/)
- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
