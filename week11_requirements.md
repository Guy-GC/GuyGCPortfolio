# Introduction

This entry will go over my attempt to create unit tests and talk about why it didn't work, and
what different problems arose for other people in the group also doing the unit testing.

# Issue for This Week

I decided to make the unit tests for this week for the calendar task. I have created the code for this
week but it has errors and a pull request hasn't been made.

``` C#
using UNDAC_App;
using UNDAC_App.Models;
using UNDAC_App.Classes;
using System.Collections.ObjectModel;
using System.Globalization;
using Xunit;

namespace CalendarTest
{
    public class UNDACCalendarUnitTests
    {
        [Fact]
        public void Test_No_Similarity_Checker()
        {
            DateTime date = new DateTime(2023, 12, 25);
            TimeSpan time = new TimeSpan(12, 0, 0);
            DateTime datetime = date + time;
            bool expected = false;
            Assert.Equal(expected, UNDAC_App.Calendar.Loop_events(datetime,1));
        }
        [Fact]
        public void Test_Delete_Checker()
        {
            DateTime date = new DateTime(2023, 10, 29);
            TimeSpan time = new TimeSpan(14, 30, 0);
            DateTime datetime = date + time;
            bool expected = true;
            Assert.Equal(expected, UNDAC_App.Calendar.Loop_events(datetime, 0));
        }
        [Fact]
        public void Test_Update_Checker()
        {
            DateTime date = new DateTime(2023, 10, 29);
            TimeSpan time = new TimeSpan(14, 30, 0);
            DateTime datetime = date + time;
            bool expected = true;
            Assert.Equal(expected, UNDAC_App.Calendar.Loop_events(datetime, 2));
        }
    }
}
```
\
I decided to make three tests; one is for a meeting that isn't in the sample meetings, one is 
for the delete option within the function, and the last is for the update option within the 
function. All of these tests are for the Loop_events function and the first test should return
false as there is no meeting that can be updated or deleted, and the other two tests should return
true.

For some reason, I wasn't able to link the unit tests with the UNDAC project. I do know of someone
else who had similar issues but they were able to link the project and the unit tests. However, when
reviewing his pull request I noticed that all of the files within the project have been renamed. Now
there weren't any actual name changes but the file location has been changed, this is when I realised the
solution for the project was changed to his local file location for the UNDAC app. This meant that although
he did get his unit tests to work, it only worked when all the files were changed to the ones on his personal
system. This would have caused lots of errors if we merged the pull request to the main.

# Summary

I did run into a lot of issues this week, I do think the unit tests would have worked if both files had been
saved on my computer. Even if it didn't work, I would still be able to troubleshoot until it did work. This
unit testing problem is pretty big as everyone within the group would also have issues trying to create unit
tests. This could lead to errors that we would realise are a problem once the app has been published and used
by users. I am again having issues with finding another issue, some people haven't attempted their issue so 
we can't do the task unless they say we can or we just brute force and just do it. Maybe we should have 
established some rules when the issues were published on the GitHub repository, but then again those people
might not care and we would still have the same problem as we do now.
