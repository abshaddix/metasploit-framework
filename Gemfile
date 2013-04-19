source 'http://rubygems.org'

# Need 3+ for ActiveSupport::Concern
gem 'activesupport', '>= 3.0.0'
# Needed for Msf::DbManager
gem 'activerecord'
# Needed for some admin modules (scrutinizer_add_user.rb)
gem 'json'
# Database models shared between framework and Pro.
gem 'metasploit_data_models', '~> 0.6.14'
# Needed by msfgui and other rpc components
gem 'msgpack'
# Needed by anemone crawler
gem 'nokogiri'
# Needed for module caching in Mdm::ModuleDetails
gem 'pg', '>= 0.11'
# Needed by anemone crawler
gem 'robots'
# For sniffer and raw socket modules
gem 'pcaprub'

group :development do
  # Markdown formatting for yard
  gem 'redcarpet'
  # generating documentation
  gem 'yard'
end

group :development, :test do
	# supplies factories for producing model instance for specs
  # Version 4.1.0 or newer is needed to support generate calls without the
  # 'FactoryGirl.' in factory definitions syntax.
  gem 'factory_girl', '>= 4.1.0'
  # running documentation generation tasks and rspec tasks
  gem 'rake'
end

group :test do
	# Removes records from database created during tests.  Can't use rspec-rails'
	# transactional fixtures because multiple connections are in use so
	# transactions won't work.
	gem 'database_cleaner'
  # testing framework
  gem 'rspec', '>= 2.12'
  # add matchers from shoulda, such as query_the_database, which is useful for
  # testing that the Msf::DBManager activation is respected.
  gem 'shoulda-matchers'
  # code coverage for tests
  # any version newer than 0.5.4 gives an Encoding error when trying to read the source files.
  gem 'simplecov', '0.5.4', :require => false
	# Manipulate Time.now in specs
	gem 'timecop'
end
