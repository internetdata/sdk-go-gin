# Changelog

What each release changed for you, newest first. Each line is a commit's summary, linked to its full description and diff.

## 1.0.10 - 2026-11-22

### Fixes

- Require golang.org/x/net 0.63.0 and golang.org/x/crypto 0.59.0 ([`50eaad2`](https://github.com/internetdata/sdk-go-gin/commit/50eaad2fbcd9b057efe2e626f3d9a9cce2d92e9a))

## 1.0.9 - 2026-11-20

### Fixes

- Say rate limit where the docs named a per-minute one ([`94eb880`](https://github.com/internetdata/sdk-go-gin/commit/94eb8802fe64ef7293738cdd93a349784d9b95c6))

## 1.0.8 - 2026-11-20

### Fixes

- Require internetdata v2.15.0: a paid domain answer's hosting, co-hosted domains, home page, redirects and backlinks ([`d5bb29b`](https://github.com/internetdata/sdk-go-gin/commit/d5bb29b83fc4c392d2e915782cba701a7645ce64))

## 1.0.7 - 2026-11-20

### Fixes

- Require internetdata v2.14.3: the spec re-pinned to 2026.11.20 ([`55925a5`](https://github.com/internetdata/sdk-go-gin/commit/55925a5fe1c33650aa8efa6fb6f4ccf332d98709))

## 1.0.6 - 2026-11-19

### Fixes

- Require internetdata v2.14.2: a reduced answer is cached a minute at most ([`b4b2e97`](https://github.com/internetdata/sdk-go-gin/commit/b4b2e97a19ea60aaa26af850b8f1a8e2cede39b6))

## 1.0.5 - 2026-11-18

### Fixes

- Require internetdata v2.14.1: the spec as republished ([`d6daeb3`](https://github.com/internetdata/sdk-go-gin/commit/d6daeb369005261d8102b15f6406b0cad9e0da5d))

## 1.0.4 - 2026-11-17

### Features

- Require internetdata v2.14.0: cap_reached on a paid answer past its overage cap ([`093e554`](https://github.com/internetdata/sdk-go-gin/commit/093e554a7c6351a279330547d78ff0be1069c9fc))

## 1.0.3 - 2026-11-16

### Features

- Require internetdata v2.13.0: an AS's rank, neighbors and hosted domains ([`e3579a3`](https://github.com/internetdata/sdk-go-gin/commit/e3579a38630b3c434810bb966ab64c7a34d01a95))

## 1.0.2 - 2026-11-15

### Features

- Require internetdata v2.12.0: hosted_domains lists its 10 most popular domains ([`4fea3ca`](https://github.com/internetdata/sdk-go-gin/commit/4fea3ca47ad7ea8cfcb572f474030e1e1d788aa0))

## 1.0.1 - 2026-11-14

### Fixes

- Require internetdata v2.11.1: a 403 can mean the key lacks the ip.lookup scope ([`fea9d88`](https://github.com/internetdata/sdk-go-gin/commit/fea9d8864db5d255a26d31b63a0baae2cd02150b))

## 1.0.0 - 2026-11-14

### Features

- Attach the visitor's InternetData record to every request's `gin.Context`, read with `FromContext`: the location, the network and the company behind the address, and the anonymity and hosting flags your plan serves ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
- Refuse a request with a `BlockCondition` written in the shape of a result, by country, network type, anonymity or any other member, with 403 or an `OnBlocked` of your own ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
- Choose where the client address comes from: gin's own `ClientIP` by default, `XFFIPSelector`, `HeaderIPSelector` for a header your edge writes, or a function of your own ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
- Fail open on any lookup failure unless `FailClosed` is set, with a 2500 ms bound, no retry and a cache per middleware by default ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
