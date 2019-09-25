# frozen_string_literal: true

clearing :on

guard :bundler

guard :rubocop, all_on_start: true

guard :rspec, all_on_start: true, cmd: 'rspec' do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$}) { |m| "spec/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb') { 'spec' }
end
