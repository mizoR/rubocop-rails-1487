```
(
    cd app
    # bundle install if not yet
    bundle exec rubocop bin/hello.rb
)
# => CI Failed

(
    cd myapp
    # bundle install if not yet
    bundle exec rubocop bin/hello.rb
)
# => CI Passed
``````

### Sample output

```
$ (                                                                                                                                                                                                                                                                                                                                                                                                   rbenv:3.4.4
    cd app
    # bundle install if not yet
    bundle exec rubocop bin/hello.rb
)
Inspecting 1 file
C

Offenses:

bin/hello.rb:3:1: C: [Correctable] Rails/Output: Do not write to stdout. Use Rails's logger if you want to log.
puts 'hello world'
^^^^

1 file inspected, 1 offense detected, 1 offense autocorrectable



$ (                                                                                                                                                                                                                                                                                                                                                                                                   rbenv:3.4.4
    cd myapp
    # bundle install if not yet
    bundle exec rubocop bin/hello.rb
)
Inspecting 1 file
.

1 file inspected, no offenses detected
```
