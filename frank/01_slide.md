!SLIDE
.huge Frank  

!SLIDE full-page-image
![frankenstein](image_frankenstein.jpg)

!SLIDE
# Work by <br>stick many <br>pieces together #

!SLIDE
# How It Works #

!SLIDE small
## 1. UISpec ##
### Query and validate ###

    @@@ c
    -(void)itShouldAddAUser {
      [app.navigationButton touch];

      [[app.textField placeholder:@"Username"] setText:@"bkuser"];
      [[app.textField placeholder:@"Password"] setText:@"test"];
      [[app.textField placeholder:@"Confirm"] setText:@"test"];
        
      [[app.navigationButton.label text:@"Save"] touch];
      [app timeout:1].alertView.should.not.exist;

      [[app.tableView.label text:@"Brian Knorr"] should].exist;
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
        
!SLIDE left incremental
## Why Frank?
- Use Ruby and Cucumber
- Record Video
- Integrates with CI
- Great Community

!SLIDE
# [testingwithfrank.com](http://www.testingwithfrank.com/)
