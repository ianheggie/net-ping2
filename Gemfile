source 'https://rubygems.org'

# Specify your gem's dependencies in net-ping2.gemspec
gemspec

group :test do
  gem "rcov", ">= 0", :platforms => :mri_18
  gem "simplecov", "~> 0.7.1", :require => false, :platforms => :ruby_19
  if File.exist?('.idea') or File.exist?('nbproject') or File.exist?('.project') or File.exist?('.settings')
    # required for ruby-mine and other IDE's, but fails to install under travis-ci
    gem 'ruby-debug-ide', '0.4.23.beta1', :platform => :ruby_19
  end
  #gem 'coveralls', :require => false, :git => 'git://github.com/ianheggie/coveralls-ruby.git'
  #if RUBY_VERSION =~ /^1\.8/
  #  # coveralls requires rest-client, but 1.7+ versions require ruby 1.9.3
  #  gem 'rest-client' , '~>1.6.8'
  #end
end
    
group :development do
  platforms :ruby do
    # not jruby
    gem "travis", ">= 1.6.0"
    gem "travis-lint", ">= 0"
  end
  if RUBY_VERSION =~ /^1\.8/
    gem 'rake', '< 10.2.0'
    # mime-types 2.0 requires Ruby version >= 1.9.2
    gem "mime-types", "< 2.0"
  else
    gem 'rake'
  end
end
