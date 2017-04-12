# PintosProject3
This is the 3rd Project for the Pintos Problem

This is where we will be documenting our steps and thought processes.

//////////////////////////////////////////////////MEMORY MAPPED FILES///////////////////////////////////////////////////////////////
Changes made to syscall.c:

In the munmap function:

I created a mapping variable, allocated space for it, and then used the given parameter to lookup the mapping that we are working with and immediately passed that over to the unmap function.

In the unmap function:

This was a bit more difficult. I researched quite a bit to find out what all was needed for this and found that I needed to deallocate the pages that were mapped, which thankfully was found in page.c. When doing that, I was told to make sure to do this for ALL pages, so I created a for loop that walked through all possible pages. Initially attempted a While Loop, but it seemed to not like going backwards when deallocating pages. After that, I made sure to remove the mapping element from the list that it was a part of. Lastly, I freed up the given parameter variable that we had made from munmap.
///////////////////////////////////////////////END OF MEMORY MAPPED FILES////////////////////////////////////////////////////////////
