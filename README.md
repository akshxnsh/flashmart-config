# flashmart-config

Tunable values for the FlashMart services, served by the monorepo's `config-server`.
One file per service, named `{spring.application.name}.yml`.

This repo is PUBLIC. It holds numbers only: timeouts, attempts, rate limits, fees.
Never a secret, a password, a DB URL, a port or a host address. Those stay in each
service's local config or in environment variables.

Each service keeps its own local copy of every value here as a fallback; the copy
here wins when config-server is reachable. Keep the two in step by hand.
