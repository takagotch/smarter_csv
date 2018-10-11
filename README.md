### smarter_csv
---
https://github.com/tilo/smarter_csv

https://github.com/tilo/smarter_csv/wiki

```
gem install smarter_csv
gem 'smarter_csv'
bundle
gem install smarter_csv

gem install smarter_csv
```
```ruby
camelcase_headers = Proc.new {|headers|
  headers.map{|x| x.strip.downcase.gsub(/(\s|\-)+/, '_').split('_').map(&:capitalize).join }
}
options = {
  header_transformations: [:none, camelcase_headers ]
}
data = SmarterCSV.process('/tmp/test.csv', options)
  => [{"Category"=>"Red", "FirstName"=>"John", "Age"=>"35"}]


```

