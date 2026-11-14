# Changelog

What each release changed for you, newest first. Each line is a commit's summary, linked to its full description and diff.

## 1.0.1 - 2026-11-14

### Fixes

- Require internetdata v2.11.1: a 403 can mean the key lacks the ip.lookup scope ([`fea9d88`](https://github.com/internetdata/sdk-go-gin/commit/fea9d8864db5d255a26d31b63a0baae2cd02150b))

## 1.0.0 - 2026-11-14

### Features

- Attach the visitor's InternetData record to every request's `gin.Context`, read with `FromContext`: the location, the network and the company behind the address, and the anonymity and hosting flags your plan serves ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
- Refuse a request with a `BlockCondition` written in the shape of a result, by country, network type, anonymity or any other member, with 403 or an `OnBlocked` of your own ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
- Choose where the client address comes from: gin's own `ClientIP` by default, `XFFIPSelector`, `HeaderIPSelector` for a header your edge writes, or a function of your own ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
- Fail open on any lookup failure unless `FailClosed` is set, with a 2500 ms bound, no retry and a cache per middleware by default ([`c8d1e3c`](https://github.com/internetdata/sdk-go-gin/commit/c8d1e3c5d538d4d26f09b36aa126d93a36650c58))
