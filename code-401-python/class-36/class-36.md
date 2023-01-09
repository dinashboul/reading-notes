# Data Fetching in React

## What is SWR?

### stands for stale-while-revalidate, a HTTP cache invalidation strategy popularized by HTTP RFC 5861. It basically means that it performs data fetching in 3 steps:

- Returns cached data first (stale)

- Sends the fetch request (revalidate)

- Returns the up-to-date data

## Why use SWR?

### Built-in Cache + Real-Time Experience:

**Using SWR’s strategy, the user sees the cached (stale) data first and requests are automatically being cached.**

### Auto Revalidation

**SWR can also revalidate data on interval, to make sure multiple sessions will render the same components based on the data.**

###  Pagination

**SWR its supports pagination and infinite loading of data.**

### More Features + Benefits of SWR

- Local mutation

- Dependent fetching

- Smart error retry

- Supports fetching from both REST and GraphQL APIs

- Typescript and React Native ready

**It is lightweight and backend agnostic, which allows fetching data from any kind of API or database quickly and easily.**

### Features

- Fast, lightweight and reusable data fetching

- Built-in cache and request deduplication

- Real-time experience

- Transport and protocol agnostic

- SSR / ISR / SSG support

- TypeScript ready

- React Native



