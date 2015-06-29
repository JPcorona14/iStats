iStats [![Gem Version](https://badge.fury.io/rb/iStats.svg)](http://badge.fury.io/rb/iStats)
======

iStats is a command-line tool that allows you to easily grab the CPU temperature, fan speeds and battery information on OS X. If you'd like to see more data available feel free to open an issue.

## Installation

    $ gem install iStats

#### Warning
**This is now fixed with the release of OS X 10.9.3**<br>
A [bug in Ruby](https://bugs.ruby-lang.org/issues/9624) and Apple XCode 5.1 onwards (new CLANG version) might make it impossible to install this gem if you are using Ruby from the Xcode command-line tools package. If you see an error when the gem is building the native extension try to use this command to install iStats: <br>
`sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future gem install iStats`<br>
If you are using RVM or homebrew to manage your Ruby installation you should be fine.


## Screenshot
#### All Stats
![](http://i.imgur.com/c4xLB8u.png)

#### Sparkline levels
![](http://i.imgur.com/ht2NZCL.gif)

## Usage

```
  - iStats: help ---------------------------------------------------

  istats --help                            This help text
  istats --version                         Print current version

  istats all                               Print all stats
  istats cpu                               Print all CPU stats
  istats cpu [temp | temperature]          Print CPU temperature
  istats fan                               Print all fan stats
  istats fan [speed]                       Print fan speed
  istats battery                           Print all battery stats
  istats battery [health]                  Print battery health
  istats battery [cycle_count | cc]        Print battery cycle count info
  istats battery [temp | temperature]      Print battery temperature
  istats battery [time | remain]           Print battery time remaining
  istats battery [charge]                  Print battery charge
  istats battery [capacity]                Print battery capacity info

  for more help see: https://github.com/Chris911/iStats
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

#### Tested on
MacBook Pro 2012<br>
OS X 10.9.3<br>
Ruby: 1.9.3, 2.0.0, 2.1.1<br>
