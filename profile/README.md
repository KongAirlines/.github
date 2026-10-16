# KongAirlines

KongAirlines is the public, working implementation of the
[Konnect Reference Platform](https://developer.konghq.com/konnect-reference-platform/).
It demonstrates federated APIOps with supported `kongctl` and decK declarative
configuration on one default branch.

The Platform Team owns shared Konnect foundations and production Gateway
governance in [`platform`](https://github.com/KongAirlines/platform). Service
teams own their API contracts, Catalog resources, and development Gateway state:

- `customer-data`: [`bookings`](https://github.com/KongAirlines/bookings) and
  [`customer`](https://github.com/KongAirlines/customer)
- `flight-data`: [`destinations`](https://github.com/KongAirlines/destinations)
  and [`flights`](https://github.com/KongAirlines/flights)

Bookings and Customer Information demonstrate Key Auth plus platform-owned
global Access Control Enforcement. Destinations and Flights remain anonymous.
CI materializes the generated Gateway configuration in each service PR so
reviewers see the exact state that will be synchronized. Each service writes
independently to its team development control plane; exact production Gateway
artifacts are promoted to the Platform Team for review and one aggregate
synchronization.

## Security

See [Security](SECURITY.md) for information on how to report security vulnerabilities.
