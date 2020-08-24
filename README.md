# lockfile

This shard implements a portable lockfile implementation. It is a port, with some modernizations, of the implementation found in the IOWA web framework for Ruby, which was, in turn, originally based on lockfile.rb from Ara Howard.

https://github.com/wyhaines/iowa/blob/master/src/iowa/Lockfile.rb

It uses links to implement atomic, portable locking, but it can fall back on the flock() call if ran in an environment where linking doesn't seem to work. This is the default mode of operation. If one specifically wants it to use only
flock, or only links, that can be specified when a lockfile is created.

## Installation

1. Add the dependency to your `shard.yml`:

   ```yaml
   dependencies:
     lockfile:
       github: wyhaines/lockfile
   ```

2. Run `shards install`

## Usage

```crystal
require "lockfile"
```

TODO: Write usage instructions here

## Development

TODO: Write development instructions here

## Contributing

1. Fork it (<https://github.com/your-github-user/lockfile/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Contributors

- [Kirk Haines](https://github.com/wyhaines) - creator and maintainer
