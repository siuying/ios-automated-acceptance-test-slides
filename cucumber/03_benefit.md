!SLIDE

.huge BDD

!SLIDE

.bigger Behavior Driven Development

!SLIDE
# Describe how software should work in code #

!SLIDE
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
