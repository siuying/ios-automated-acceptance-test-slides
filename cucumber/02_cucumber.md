!SLIDE small
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

!SLIDE
## 2. Write Steps in Ruby ##
    
    @@@ ruby
    When /^I press "([^"]*)" button$/ do |name|
      calculator.press(name)
    end

!SLIDE
## 3. Run and Watch it Fail ##

    @@@ ruby
    $ cucumber

!SLIDE
## 4. Write code to make it pass ##
    
    @@@ ruby
    class Calculator
      def press(number)
        @display << number
      end
    end

!SLIDE
## 5. Run again and see it pass ##

    @@@ ruby
    $ cucumber


!SLIDE
## 6. Go to step #1 and start again

(write more features!)

!SLIDE

.huge BDD

!SLIDE

.bigger Behavior Driven Development

!SLIDE
# Describe how software should work in code #
## Not documents! ##

!SLIDE
# Human Readable #
## Your users can read it ##

!SLIDE

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

!SLIDE

.bigger Demo