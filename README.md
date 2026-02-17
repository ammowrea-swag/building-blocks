
## Ashley's Svelte Components 

For my page, I wanted to build three components
1. An accordion drop down for additional reading (a word count hates to see me coming)
2. A sidebar that allows me to add additional details without weighing down the main body content (again, a word count hates to see me coming)
3. An author box, per Ben's list of creative options 


For the accordion page, I tried to lift svelte code from an online resource directly, but it was ugly and kind of unhelpful, so I let CoPilot take the lead but did ask the robots to make the style similar to Ben's "Related Links Section." 

The drama was my autoprompted coding on the +page would invent its own labels for the different sections rather than reading the .svelte page, so I had a few attempts to correct the language differences between the two pages. 

Then, I made the sidebar, which the robot did not know to Float (like hello, that's the side part of sidebar), so had to do some stylistic tweaking there as well. Similarly, when placing it on the page, I had to double check that the div classes I had assigned to the component made it onto the page.

For the author box, I went back to plagarizing from Google (I have no robot loyalty). That was mostly successful, until it came to styling it. But this component was a simpler process to refine (I cut a suggested twitter account link from the author box), I think because it was fewer  mechanisms; just name, bio and photo.

My worst flop was forgetting to add the components to the script section of my page, CoPilot had to help me with that thrice even tho I made it to a 505 error each time. 