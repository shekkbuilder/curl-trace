# curl-trace
an opinionated way to run curl that gives you output formatting like this:

```
Request Details:
            url: https://www.google.com/
  num_redirects: 0
   content_type: text/html; charset=ISO-8859-1
  response_code: 200
      remote_ip: 216.58.193.100

Timing Analysis:
     time_namelookup: 0.137
        time_connect: 0.193
     time_appconnect: 0.437
    time_pretransfer: 0.437
       time_redirect: 0.000
  time_starttransfer: 0.536
                      ----------
          time_total: 0.730
```

## Installation

Clone the repo locally.

```
git clone git@github.com:wickett/curl-trace.git
```

Add `alias curl-trace='curl -w "@/path/to/repo/templates/.curl-format" -o /dev/null -s'` to your `.bash_profile` to get timing and other analysis for your curls.

Reload `.bash_profile`

```
source ~/.bash_profile
```

## Usage

```
$ curl-trace -L https://google.com
```

```
$ curl-trace https://www.google.com/

Request Details:
            url: https://www.google.com/
  num_redirects: 0
   content_type: text/html; charset=ISO-8859-1
  response_code: 200
      remote_ip: 216.58.193.100

Timing Analysis:
     time_namelookup: 0.137
        time_connect: 0.193
     time_appconnect: 0.437
    time_pretransfer: 0.437
       time_redirect: 0.000
  time_starttransfer: 0.536
                      ----------
          time_total: 0.730

```

## Suggestions for additional templates
Open an issue or send a pull request. It would be great to have a collection of templates for running curl.


