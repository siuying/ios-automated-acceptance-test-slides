!SLIDE
.huge Frank

!SLIDE full-page-image
![frankenstein](image_frankenstein.jpg)

!SLIDE
# Work by <br>stick many <br>pieces together #

!SLIDE
# How It Works #

!SLIDE
## 1. UISpec ##
### Query and validate ###

    @@@ c
    -(void)itShouldNotAddAnInvalidUser {
      [app.tableViewCell touch];
      [app.label.should.have text@"User Profile"];
    }

!SLIDE full-page-image
## 2. Embedded web server ##
![](symbiote.png)

!SLIDE full-page-image
# 3. Driver (frank-cucumber) #
## Control iOS from Ruby ##

!SLIDE small
## 4. Executable test in cucumber ##

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
        
!SLIDE incremental
## Why Frank?
- Use Ruby and Cucumber
- Record Video
- Integrates with CI
- Great Community

