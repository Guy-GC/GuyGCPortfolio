# Introduction

This entry will go over the addition of the NoOverlap function to make sure two or more events don't run at the same time
or overlap. I will also go over all the pull requests I commented on and what changes I suggested for those pull requests.

# Issue For This Week

I decided to continue and finish the calendar issue by adding a function that detects events that overlap with one another.
This function will be used when an event is created or updated, it doesn't need to be used for deleting an event as it 
can't overlap with another event if it doesn't exist. This is a code snippet of the NoOverlap function:

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2315.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.1 - New NoOverlap function</b>
</figcaption>
</figure>

\
I decided to use a for each statement when looping through all the meetings as there is less to write with a for each statement than a
for statement with an integer that goes through each element within the list. This is a good example of the DRY principle
as it keeps the code a little simpler by reducing the number of characters, it makes the code look a lot easier to understand,
and it still does the same as a regular for loop. I also made sure that if a meeting ends at 4 PM and another one starts at
4 PM that this isn't considered an overlap.

I have also used other good coding principles like good commenting. I have made a summary of the function explaining what
it does, and only used comments within the function whenever some bits of code needed a little explaining.

I made the function a bool for the same reason the LoopEvent function is also a bool. I used if statements that refer to the
function as shown below:

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2316.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.2 - NoOverlap call in If Statement in LoopEvents function for Updating Events</b>
</figcaption>
</figure>

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/CodeCapture%2317.PNG"
width="100%" alt="drawing" />
<figcaption <b>Fig.3 - NoOverlap call in If Statement in AddEvent function</b>
</figcaption>
</figure>

# Code Review

My code review was very positive with one little fix to do. here is the code review

```
Nice quality of life addition to the calendar feature. Code looks good and clean, no code smells exhibited and KISS, DRY and YAGNI seem to have been followed. Only suggestion/comment is that the code comments aren't exactly necessary as the code is self describing, but that is more of a subjective choice.

I would also suggest the No_overlap function name should follow PascalCase as per C# coding convetions, and so should be No_Overlap or even OnNoOverlap potentially.

Other than that the function is clearly laid out and written, the parameters are suitable and it is of an appropriate length, while only dealing with one thing.
```
\
This was a simple fix and was sorted within minutes, the names of each functions being PascalCase, and some comments remove as they were
redundant.

The code review I did for someone else had one small fix it could of done. The code didn't have any summaries and not a lot
of commments. Here is an example:

```C#
private void OnEquipmentDeleted(object sender, EventArgs e)
{
        var button = sender as Button;
        var selectedEquipment = button?.CommandParameter as Equipment;

        if (selectedEquipment != null)
        {
            equipmentManager.DeleteEquipment(selectedEquipment.Id);

            EquipmentList.Remove(selectedEquipment);
        }
}
```
\
I suggested to add summaries to make the code more understandable without having to overcommment within the blocks of code
it self

I'm going to go over all the code reviews I did for other people's issues with the provided original code and then my suggestion
for what to change in their code. The first change I suggested for a code was to remove an extra else statement. Here is the original
code for the issue:

``` C#
 public bool CheckUserAccess(int userID)
        {
            UserLoggins userToCheck = connection.Table<UserLoggins>().FirstOrDefault(b => b.ID == userID);
            if (userToCheck != null)
            {
                if (userToCheck.User_Access == "Granted")
                {
                    return true;
                }
                else
                {
                    return false;
                }
            }
            else
            {
                return false;

            }
        }
```
\
I suggested to either get rid of the first else statement like so:

``` C#
 public bool CheckUserAccess(int userID)
        {
            UserLoggins userToCheck = connection.Table<UserLoggins>().FirstOrDefault(b => b.ID == userID);
            if (userToCheck != null)
            {
                if (userToCheck.User_Access == "Granted")
                {
                    return true;
                }
            }
            else
            {
                return false;
            }
        }
```

\
Or to use a & operator within the first if statement like so:

``` C#
 public bool CheckUserAccess(int userID)
        {
            UserLoggins userToCheck = connection.Table<UserLoggins>().FirstOrDefault(b => b.ID == userID);
            if (userToCheck != null && userToCheck.User_Access == "Granted")
            {
                return true;
            }
            else
            {
                return false;
            }
        }
```
\
This would be a better example of the KISS principle as it removes the redundant else statement and gets rid
of the second if statement. It could technically be using the DRY principle as it repeats an if statement that
can be used just within the first if statement. There were other examples within the code that does something
similar with two lines that return the bool function as false.

Another example of code review with a suggestion I made was the following:

``` C#
	private async void OnAddSubTeamStatusClicked(object sender, EventArgs e)
	{
		var newStatus = new SubTeamStatus();
		newStatus.subTeamName = await DisplayPromptAsync("New Sub Team Status", "Please enter the Sub Team's name");
        newStatus.status = await DisplayPromptAsync("New Sub Team Status", "Please enter the Sub Team's status");
        newStatus.issue = await DisplayPromptAsync("New Sub Team Status", "Please describe the issue");
        newStatus.resolution = await DisplayPromptAsync("New Sub Team Status", "Please describe your resolution");

		if (!string.IsNullOrWhiteSpace(newStatus.subTeamName) && !string.IsNullOrWhiteSpace(newStatus.status) &&
			!string.IsNullOrWhiteSpace(newStatus.issue) && !string.IsNullOrWhiteSpace(newStatus.resolution))
		{
			subTeamStatusManager.AddSubTeamStatus(newStatus);
			SubTeamStatusList.Add(newStatus);
		}
    }
```
\
I suggested making the code indentation a little better to the following:

``` C#
	private async void OnAddSubTeamStatusClicked(object sender, EventArgs e)
	{
		  var newStatus = new SubTeamStatus();

      newStatus.subTeamName = await DisplayPromptAsync("New Sub Team Status", "Please enter the Sub Team's name");
      newStatus.status = await DisplayPromptAsync("New Sub Team Status", "Please enter the Sub Team's status");
      newStatus.issue = await DisplayPromptAsync("New Sub Team Status", "Please describe the issue");
      newStatus.resolution = await DisplayPromptAsync("New Sub Team Status", "Please describe your resolution");

		  if (!string.IsNullOrWhiteSpace(newStatus.subTeamName) && !string.IsNullOrWhiteSpace(newStatus.status) &&
			  !string.IsNullOrWhiteSpace(newStatus.issue) && !string.IsNullOrWhiteSpace(newStatus.resolution))
      {
            subTeamStatusManager.AddSubTeamStatus(newStatus);
            SubTeamStatusList.Add(newStatus);
      }
  }
```
\
(if you look at the code within the code of the markdown file as the newStatus. lines are too big for the preview)

This improves the code readability and can result in cleaner code, by adding indentations and having some blank
space in between the variable and newStatus. lines as well as a space in between the newStatus. lines and the 
if statement.

# Summary

I ran into an issue this week merging my branch into the main branch, I created a branch that was a copy of the main
branch and then made some changes to my file. Someone decided to clean up the project by putting the XAML.cs and XAML
files into the Views folder in another folder called GreenTeamFolder. These changes were finished before I finished
my changes to the app. I created a pull request and got an approval to merge the branch but Github said that there was
a conflict in files, and that file was my Calendar.XAML.cs file which was the file I edited. When fixing the conflict
the conflicts were comparing an old version of my file with some aspects of the new file. I eventually got the conflict
to have all of my new code but when I merged the branch it merged the main branch into my branch which is very strange 
as there was no difference in the process of creating new code, making a new branch, and creating a pull request. It took
some time to fix but this was a very interesting issue. I did mention that it could be because of the file being moved into 
the Views folder, but I am still not 100% sure what the actual problem was. This probably could have been avoided if
I maybe waited till all the files have been sorted or completed the task before.
