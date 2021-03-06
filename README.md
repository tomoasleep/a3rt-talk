# A3rt::Talk

Helper for A3RT talk API

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'a3rt-talk'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install a3rt-talk

## Usage

```
api_key = "your api key"
msg = "Hello"
resp = A3rt::Talk.talk(msg, api_key)
puts resp.least_perplex.reply
```

If you talk with a3rt many times, you can `authorize!`.

```
api_key = "your api key"
A3rt::Talk.authorize!(api_key)
puts A3rt::Talk.talk("Hello").least_perplex.reply
puts A3rt::Talk.talk("Bye").least_perplex.reply
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/hkdnet/a3rt-talk.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

