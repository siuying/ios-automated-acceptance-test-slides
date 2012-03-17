!SLIDE small left
## 1. Describe Your Software ##

    @@@ ruby
    Feature: 
      As a student
      I want to input numbers to 
      calculator
      So I can calculate

      Scenario: Input Number
        Given I launch the app
        When I press "1" button
        When I press "2" button
        When I press "3" button
        Then I see "123" on display

!SLIDE left
## 2. Write Steps in Ruby ##
    
    @@@ ruby
    When /^I press "([^"]*)" button$/ do |name|
      calculator.press(name)
    end

    Then /^I see "([^"]*)" on the display$/ do |number|
      calculator.display.should == number
    end

!SLIDE small left
## 3. Run and Watch it Fail ##

    @@@ ruby
    $ cucumber
    ...
    Scenario: Input Number
      Given I launch the app
      When I press "1" button
      When I press "2" button
      When I press "3" button
      Then I see "123" on the display
        expected: "123"
        got: "" (using ==) (RSpec::Expectations::ExpectationNotMetError)


!SLIDE left
## 4. Write code to make it pass ##
    
    @@@ ruby
    class Calculator
      attr_accessor :display
      def press(number)
        @display << number
      end
    end

!SLIDE small left
## 5. Run again and see it pass ##

    @@@ ruby
    $ cucumber
    ...
      Scenario: Input Number
        Given I launch the app
        When I press "1" button
        When I press "2" button
        When I press "3" button
        Then I see "123" on the display

!SLIDE left
## 6. Go to step #1 and start again

(write more features!)
