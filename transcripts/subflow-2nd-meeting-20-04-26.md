# Subflow 02
*Generated on 4/21/2026*

---

**Marcos Briceno:** Is the one regarding the initial flow usage, but the others are all there.

**Marcos Briceno:** I guess we can maybe start with wait, let me find the channel because I lost.

**Marcos Briceno:** Okay.

**Marcos Briceno:** Yeah.

**Marcos Briceno:** So we had some questions that we couldn't get into last week, but we could, I guess we could go over those.

**Marcos Briceno:** I think they were related more to so features actually of the product.

**Audra Wallace:** Yes.

**Marcos Briceno:** Yep.

**Marcos Briceno:** Let me just open the list where I have the questions here.

**Marcos Briceno:** So some of them I think were related to like the webhooks and API.

**Marcos Briceno:** So we can leave those aside for later when we actually go over it with the team for the API.

**Marcos Briceno:** I think that.

**Marcos Briceno:** Yes, we have some.

**Marcos Briceno:** One of the white papers that we had, like the one that you guys sent was mentioning segmentation, but we really didn't understand a lot of that concept and how like it related to the, to the flows and the relationship between like the segmentation and flow.

**Marcos Briceno:** So I think we could, if you guys could go over that would be great.

**Audra Wallace:** Perfect.

**Audra Wallace:** I can start.

**Audra Wallace:** Let me share my screen.

**Audra Wallace:** All right, can everybody see?

**Marcos Briceno:** Yep.

**Audra Wallace:** So within contacts you have the ability to add what are called tags.

**Audra Wallace:** So within contacts you click on a contact under details, you have on the right hand side tags based off of these tags.

**Audra Wallace:** These are different abilities to group individuals.

**Audra Wallace:** So it could be anything from staff to a test or to say like right now we have some that they prefer English as their spoken language.

**Audra Wallace:** So you're able to add that tag and based off of that tag, when you save it, you're able to create a segment off of it.

**Audra Wallace:** So these segments are just groupings of patients and they can be based off tags or based off of answers to questions and form data.

**Audra Wallace:** So you come up and you create a new segment.

**Audra Wallace:** Let's just say this is English speaking and create the description.

**Audra Wallace:** You can come in to the different search facets and you can either combine with and or.

**Audra Wallace:** So it can be based off of different fields or different questions that we get off of all of the form data.

**Audra Wallace:** So this could be something as simple as a tag here that I'm an English speaker and I don't speak another language.

**Audra Wallace:** Or it could be like high pain.

**Audra Wallace:** So based off of a form response and I could come down here and say, I think I have it in here.

**Audra Wallace:** What is your current pain level?

**Audra Wallace:** And if it is five and you know, or four or three or two, I guess this would be low pain, the way I'm going.

**Audra Wallace:** And it can match any value.

**Audra Wallace:** So any person with a pain, a good pain score would be in here.

**Audra Wallace:** So then what I can do with that is and I could select that they are an English speaker that has pain.

**Audra Wallace:** And I'm combining those different aspects so that I can either come back in here and see this grouping of individuals.

**Audra Wallace:** I didn't end up saving it, but for this low pain I can see, okay, how many patients are in low pain?

**Audra Wallace:** Just these two versus how many patients are in high pain.

**Audra Wallace:** Okay, maybe I need to address Mitch's high pain or it could be used under broadcast.

**Audra Wallace:** So if I'm going into my messaging one to many SMS broadcast, so I need to send it to a whole group of individuals.

**Audra Wallace:** So I want to reach out to everybody that has high pain to say, let's get you on some different meds or what some of our users are using this for right now is to send out to all the English speakers that have copd.

**Audra Wallace:** Send out, hey, we have a this educational opportunity coming up versus Spanish speakers that have copd.

**Audra Wallace:** Let's send them a message, but send it in English.

**Audra Wallace:** I mean, send it in Spanish so that they can read it so that this is one way to use those groupings that we have the availability of so that we can send different messaging web or we can pull reports based off of those segments as well.

**Audra Wallace:** But segments is just a way to group patients based off of different features.

**Marcos Briceno:** Makes sense.

**Marcos Briceno:** I imagine you can trigger different things in workflows based on those segments as well, right?

**Audra Wallace:** Yes.

**Audra Wallace:** So you can use those to when a contact is added to a segment to kick off a workflow or when it's listening throughout a workflow.

**Audra Wallace:** You can use that on paths as well.

**Audra Wallace:** If they are part of this segment or have this tag go down this path versus another path as well.

**Heitor Tessaro:** And are these segments automatically updated based on the answers from the patients?

**Audra Wallace:** The segments can be updated based off of workflow changes.

**Audra Wallace:** It can be worked off of form submissions.

**Audra Wallace:** These can be so anything that's able to add or remove tags or different answers to different aspects of a patient's record that can either add or remove them from segments.

**Audra Wallace:** So they are dynamic lists.

**Audra Wallace:** So if,.

**Heitor Tessaro:** But I mean you don't need to trigger like, okay, update the database to check if someone else also match this condition.

**Audra Wallace:** It automatically pulls them in to segments based off of the the contact record changing.

**Audra Wallace:** Okay, and then I could have it remove the patient from the segment.

**Audra Wallace:** I could have a workflow action that says once Audra completes the task to address high pain, remove Maddie from the segment so that it removes her because it's already been addressed and I need her off of that segment.

**Audra Wallace:** So that that segment is live and active.

**Audra Wallace:** Or if.

**Audra Wallace:** If Maddie answers another questionnaire and she updates her pain now to 1 instead of a 9, it would remove her from that segment because her answer is no longer a nine, she no longer meets the criteria to be in that segment.

**Heitor Tessaro:** Got it.

**Heitor Tessaro:** But what if you remove someone from the segment but the condition that was triggered to include that person in this segment continues through.

**Audra Wallace:** I would need to change the trigger that adds into the segment, because I do not add a person.

**Audra Wallace:** I don't come in here and add a person to the segment.

**Audra Wallace:** I change the conditions that the segment is based off of.

**Heitor Tessaro:** Okay, so when you are removing this person from the segment, you need to remove the condition that.

**Audra Wallace:** Yes.

**Heitor Tessaro:** Okay.

**Audra Wallace:** I change the.

**Audra Wallace:** So, like, if I was removing me from high risk, I would either have a workflow value or I would come into their contact that removes high risk, and when it's saved, I would be removed from the segment.

**Audra Wallace:** But it's all based off of the conditions of the patient.

**Audra Wallace:** So I am not technically physically adding patients to or removing them from segments.

**Audra Wallace:** I am changing the contact record conditions to either meet or not meet the conditions of the segment.

**Heitor Tessaro:** Got it.

**Heitor Tessaro:** So in the case of the.

**Heitor Tessaro:** In the high pain case, you basically need to.

**Heitor Tessaro:** You need to reset the value, Right?

**Audra Wallace:** Correct.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** Got it.

**Audra Wallace:** And that can either be done manually by me or when I complete a task that then changes the patient's pain level back to zero.

**Audra Wallace:** Or there's a couple different ways to get to that.

**Audra Wallace:** I can come directly into the contact record or the workflow can handle changing that based off of actions that have been taken.

**Heitor Tessaro:** Right.

**Heitor Tessaro:** Okay.

**Audra Wallace:** And the segments, like I said, can be used to affect paths taken.

**Audra Wallace:** Reports can be taken off of them, and their primary.

**Audra Wallace:** One of the primary uses right now for them is to be able to send the broadcast messaging so that they can reach.

**Audra Wallace:** And those don't create a group text.

**Audra Wallace:** It still goes.

**Audra Wallace:** Like, I sends an individual message, just like the workflow does, but I can send it to a lot of people at one time so that I'm not sending a ton of different individual messages.

**Heitor Tessaro:** Got it.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** I think that it's clear.

**Marcos Briceno:** There was another concept on the file, which was the referrals and referral coordination.

**Marcos Briceno:** We also wonder how that worked with.

**Marcos Briceno:** I didn't go over it on last week.

**Audra Wallace:** Yeah.

**Audra Wallace:** So this is a feature that has been somewhat placed on the back burner from, like, a full coordination of the referrals.

**Audra Wallace:** Right now, the primary way we're doing that is through forms.

**Audra Wallace:** So in the form Submissions the way they're asking the questions of who were you referred from and what is that person's information?

**Audra Wallace:** All that is being gathered on the forms.

**Audra Wallace:** But that is there's plan on our, on our roadmap there's a plan for a more robust referral feature where I am a primary care physician that is referring to a specialty pulmonologist and my contact record is able to live amongst all of them so that I can see the records off of theirs and they're able to see it sort of an information share.

**Audra Wallace:** But that is not something that is currently built.

**Audra Wallace:** So it's not something that I can really speak to yet because still in the pre brain creation even at this moment.

**Marcos Briceno:** But the idea would be like if a patient is referred to another MD then they can basically share the information.

**Marcos Briceno:** The other MD can like have a follow up on like how was the console, was everything well and like know what's happening with.

**Marcos Briceno:** With their patient.

**Queendoline Akpan:** Right.

**Audra Wallace:** And at, at some point our vision for this feature would be that like if you've created.

**Audra Wallace:** So as a primary care physician I have the patient's intake form.

**Audra Wallace:** When you go over to the pulmonologist, why are you filling out most of the same questions?

**Audra Wallace:** Yeah, all over again.

**Audra Wallace:** Maybe the pulmonologist has 10 extra new questions but the pulmonologist questionnaire should be the whole questions or the whole list of 120 questions but only 10 of them are new.

**Audra Wallace:** So the primary care form should flow into that form.

**Audra Wallace:** So those are sort of pre filled and can be confirmed by the patient rather than having to be completely filled out again.

**Audra Wallace:** But then it has the open new questions for the patient to fill out.

**Audra Wallace:** But so the information is still being confirmed by the patient but it's saving so much time and creating improved accuracy because if the patient updates something over here, it would alert the primary care that something new has happened according to your form.

**Audra Wallace:** But then it also saves the patient a ton of time so that you're not answering the same stupid questions a million times.

**Marcos Briceno:** And and this will be still applicable if the, if the patient needs like more than one specialist at some point.

**Marcos Briceno:** Like if he goes it will be shared across all of them all the.

**Audra Wallace:** Once again our vision for this was like with our ambulatory surgery centers, the surgeons that referred or like that work at the surgery center and then on the other side the physical therapists that treat the patient after and then it could even go back okay, there's the orthopedic surgeon that's going into that.

**Audra Wallace:** But then behind there is the primary care physician that referred them to the orthopedic surgeon.

**Audra Wallace:** From there, there's also imaging that needs to get the information back in.

**Audra Wallace:** So if there was a way that they could all, you know, our vision for this is that they all have subflow accounts and the patient information is able to be securely shared across those because right now one is they're all on different EHRs and the information isn't shared and then nobody knows what the other person has and what they were shared.

**Audra Wallace:** And all of that information could be more easily flow through and then the patient.

**Audra Wallace:** Also, instead of having to arrive 45 minutes before your appointment to fill out paperwork, your paperwork's already done and can just be updated along the way.

**Audra Wallace:** And then it also keeps it more accurate because when you see the physical therapist and you're not going back to the PCP for another six months, well, the information that you fill out on the therapist forms is being updated into the pcp.

**Audra Wallace:** So if there's something that needed to be addressed of a new cardiac condition or a new, you know, whatever it may be, all of that information would be shared and coordinated to save time and increase accuracy.

**Audra Wallace:** So but like I said, that's a not current situation.

**Audra Wallace:** That's a vision.

**Audra Wallace:** That's our backlog.

**Marcos Briceno:** Yeah, I think that we can even.

**Marcos Briceno:** Because in regards to other questions that we have, I think I have the markers on the answer, but it's because we didn't directly add the question.

**Marcos Briceno:** But you actually answered them while you were explaining everything last week.

**Marcos Briceno:** Yeah, but we going to the backlog thing and think it will be important for us to map like what feature should we document first.

**Marcos Briceno:** Yeah, because I see that there are a lot of things that are like not yet completely done.

**Marcos Briceno:** Yeah, exactly.

**Heitor Tessaro:** So we should prioritize.

**Audra Wallace:** The biggest thing for me is if when our users right now are primarily using form submissions, the texting and email communication that broadcast goes along with, they are potentially editing contact cards and like adding context to the system and then tasks.

**Audra Wallace:** So we can start with those.

**Audra Wallace:** Like, I had two different people message me this morning asking, hey, I forgot how I think I messed up this broadcast.

**Audra Wallace:** How do I create a new broadcast?

**Audra Wallace:** So if our first level of documentation could be for our current users to just be, how do I create a broadcast?

**Audra Wallace:** How do I view a broadcast?

**Audra Wallace:** How do I know what was sent?

**Audra Wallace:** How do I look at a form submission?

**Audra Wallace:** How do I complete a task or create a task?

**Audra Wallace:** They are not necessarily creating fields and forms and creating workflows and creating the care plans Right now.

**Audra Wallace:** So.

**Audra Wallace:** So I think the most immediate would be the documentation for our current users of how to use the features that are being most used so that I can send them that documentation.

**Audra Wallace:** Because I just hopped on Loom and created a quick screen recording and sent it over to them and they've already emailed me back with, you know, questions or whatever.

**Audra Wallace:** So that would be my preference of sort of a starting point for us.

**Heitor Tessaro:** Sure, I think that we can do that.

**Marcos Briceno:** Maybe.

**Heitor Tessaro:** You can go through these options and explain what we should cover for each one.

**Heitor Tessaro:** Just.

**Heitor Tessaro:** Vanjie, don't you have questions about forms?

**Heitor Tessaro:** But maybe we can.

**Heitor Tessaro:** Yeah, I don't remember.

**Heitor Tessaro:** I lost.

**Evangelina Sorello:** Yeah, the like on our last call you were showing us that informs they were from the contacts.

**Evangelina Sorello:** What you call these like are these applications the different.

**Audra Wallace:** Yeah, it could be different.

**Audra Wallace:** Yeah.

**Audra Wallace:** Different apps or different features or.

**Audra Wallace:** I'm trying to think.

**Audra Wallace:** Mitch called it something the other day that made more sense.

**Audra Wallace:** But yeah, these are sort of the different applications that can be used throughout.

**Audra Wallace:** I think that's fine.

**Evangelina Sorello:** Okay.

**Evangelina Sorello:** Yes, because it's nice for us to know which, you know, label you use.

**Evangelina Sorello:** So also like patients or users.

**Evangelina Sorello:** Exactly.

**Evangelina Sorello:** Know what we are all addressing and calling.

**Evangelina Sorello:** Yeah, that's great.

**Evangelina Sorello:** So here you were mentioning that you add contact fields and this is how you, let's say what you use to create the forms.

**Evangelina Sorello:** So one of my questions was if you need to add these fields manually or if you can do it, there is like an automated process.

**Evangelina Sorello:** I don't know when you collect data from the different centers or how, how you do it in which way.

**Audra Wallace:** Yeah.

**Audra Wallace:** So right now when we get a new form, an intake form from a client, I come in and I create these contact fields.

**Audra Wallace:** So I come up to the right hand corner and say create field.

**Audra Wallace:** I think I showed this, but I select, I can select groups, I can ask a question, add in a description for them that will be visible to the user in columns.

**Audra Wallace:** And then I come over here and I can select which field type.

**Audra Wallace:** And this I'm going to just allow as a single line text.

**Audra Wallace:** And then I'm not going to create or set any specific rules, but I can here and then I can preview it here.

**Audra Wallace:** So this is what the form field will look like.

**Audra Wallace:** And if I create that, then I can come into and I, I go through and I create all of the questions.

**Evangelina Sorello:** Yeah.

**Evangelina Sorello:** So these are created manually?

**Audra Wallace:** Yes.

**Evangelina Sorello:** Okay.

**Audra Wallace:** At some point we will have templated pre made fields according to FHIR standards.

**Audra Wallace:** We've started to create those that would be able to Be like uploaded into the system as like a starter pack.

**Evangelina Sorello:** Type thing maybe then they can edit if they need.

**Audra Wallace:** Yeah, they can make it their own versus having to create fully.

**Audra Wallace:** But right now we are creating mostly Joshua and I create these fields and then come into forms and I can create a form.

**Audra Wallace:** And when I create a form, I can name it here.

**Audra Wallace:** Okay, I can change the name of the button level, the submit button.

**Audra Wallace:** I can tag these so that they're more easily searchable.

**Audra Wallace:** I typically leave this as where it is selected, where it will create or update contact fields so that this form can edit the contact information.

**Audra Wallace:** Because that's how it would add it to a segment or remove it from a segment.

**Audra Wallace:** And right now we're keeping forms public.

**Audra Wallace:** But you can choose if they are public and be able to anyone with the link or if they are private only to the individual that it was sent to.

**Audra Wallace:** Then I.

**Audra Wallace:** It starts off with these sort of predefined fields that are in all of our questionnaires.

**Audra Wallace:** But then I can come over on the right hand side and it starts off with it in settings.

**Audra Wallace:** But if I press fields here, then I can search for my contact field that I just created or I can scroll down through and you can see these headings.

**Audra Wallace:** So this is why it's easier if I'm creating.

**Audra Wallace:** I can see where my grouping is for onboarding.

**Audra Wallace:** Here it is right here.

**Audra Wallace:** I can either press on the not used button and you see the green dot or the green plus shows up.

**Audra Wallace:** If I click it adds it automatically to the bottom of the form.

**Audra Wallace:** If I want to drag it specifically to a particular spot, then if I grab the nine dots I can drag it and place it wherever I want and it puts it on top here.

**Audra Wallace:** Once it's on here, if I want to change the positioning, I just select the question and I can always grab the hand to move it around as well.

**Evangelina Sorello:** Can you create like sections?

**Audra Wallace:** There is the ability within settings to create different steps.

**Audra Wallace:** So this creates.

**Audra Wallace:** Whenever I'm looking at the form page, it has different.

**Audra Wallace:** It's paginated so I can add a second step here and a description and it creates the other steps here so that I can see.

**Audra Wallace:** Step one has these questions.

**Audra Wallace:** Step two, when I go back to fields here, I can select different here and I can do as many steps as wanted here.

**Audra Wallace:** Within the form here.

**Audra Wallace:** Once this is selected once again, I can change the exact wording.

**Audra Wallace:** If I realize that oh, for this particular form I actually want this to be.

**Audra Wallace:** I want this to have the descriptor here I can Add in placeholders ahead of time.

**Audra Wallace:** If I want, I can add in default values.

**Audra Wallace:** I can change the field size so that changes how large it is here.

**Audra Wallace:** And then I can change which step it's in.

**Audra Wallace:** So which over here.

**Audra Wallace:** If I realize that I actually want it in step two instead of having I can't drag and drop to another step, so instead I would change it here to step two and it moves the question here.

**Audra Wallace:** And then I can drag and drop it to change it over here.

**Evangelina Sorello:** Right?

**Audra Wallace:** In addition, I can create different rules.

**Audra Wallace:** So if I open here, I can require that field so that you cannot go on to the next step or submit the form without filling in this answer.

**Audra Wallace:** And then if it is a fill in the blank option, I can set min or max character limits.

**Audra Wallace:** Allow numbers only.

**Audra Wallace:** Don't you know I can make.

**Audra Wallace:** I can change this specifications versus if it was a field like maybe you can combine like.

**Evangelina Sorello:** Like a description of the feel like only numbers and then add the only numbers Validation, let's say yes.

**Audra Wallace:** So if I have a different character limits, I can specify those specific character limits.

**Audra Wallace:** If I want to not allow special characters, I can do that there.

**Audra Wallace:** If we're back over the weight again, when I allow numbers only, I can set number value min and max instead of character limits.

**Evangelina Sorello:** Yeah.

**Audra Wallace:** And then for field visibility, we have the ability to hide the field completely.

**Audra Wallace:** So if this is just an informational thing, what that I want to see or that I'm using to trigger a workflow based off of or a piece of data like that I want to see this form was submitted.

**Audra Wallace:** We're doing this sometimes with if I only want information off of this form, if it was the first time this form was ever submitted, I might create a field that says like first time so that I know that this form when it was submitted was the very first time.

**Audra Wallace:** Because then I can reset that at a point so I can hide fields or I can do conditional displays.

**Audra Wallace:** So for the conditional display, I have to select a controlling field and then the condition.

**Audra Wallace:** So any of and then select the values.

**Audra Wallace:** So this is a little bit.

**Audra Wallace:** Let's see, State one of my options.

**Audra Wallace:** Okay, actually let's do this.

**Audra Wallace:** I only want to know their weight if they are from Alabama.

**Evangelina Sorello:** So sorry there.

**Evangelina Sorello:** But I see that you have only two options for the condition field.

**Evangelina Sorello:** Where did you create those options?

**Audra Wallace:** Yes, so sorry.

**Audra Wallace:** Those controlling fields are any fields in the form that have options that I can select from.

**Audra Wallace:** So if it is a fill in the blank field, it cannot be a conditional display because I can't Account for all the different options.

**Audra Wallace:** Right.

**Audra Wallace:** So if I'm going to create if I need a controlling field, it has to be either a dropdown, a multi select or a yes no selection.

**Audra Wallace:** It has to be firm values that can be predetermined.

**Audra Wallace:** Does that make sense?

**Evangelina Sorello:** Yeah.

**Evangelina Sorello:** And also created in the contact field with the.

**Audra Wallace:** Yeah.

**Audra Wallace:** So those and these controlling fields have to be on this form so that it's something that I can make this visible when that is met.

**Audra Wallace:** Because if I have.

**Audra Wallace:** Let's see, maybe not that one.

**Audra Wallace:** Okay.

**Audra Wallace:** So now you can see when I go back to the field visibility I can see there's additional options because I at there are more questions on this form that this could be hidden or made viewable for.

**Evangelina Sorello:** Okay.

**Audra Wallace:** Because if I select okay, I only want this to be visible if they're from Alabama.

**Audra Wallace:** So if they selected Alabama here and.

**Audra Wallace:** You know, or if I came and said how would you rate the anesthesia?

**Audra Wallace:** If it's A1, then I want this field to be visible because what that looks like in practice, then let's go back to the state because I know that I'll be able to remember that I selected Alabama when I say oh,.

**Heitor Tessaro:** Oh.

**Audra Wallace:** And the controlling field has to be required, I believe.

**Audra Wallace:** Because in order to make this viewable or not, this one has to be selected on the form and you, you.

**Evangelina Sorello:** Can only apply one condition.

**Evangelina Sorello:** Perform or you can apply more than one.

**Audra Wallace:** You can apply.

**Audra Wallace:** Hold on just a second.

**Audra Wallace:** Like this is visible when this one question is there?

**Audra Wallace:** Yeah.

**Audra Wallace:** One controlling field at this time.

**Evangelina Sorello:** One controlling field.

**Audra Wallace:** Yeah.

**Audra Wallace:** Whereas when we're in workflows there's a lot of and ors.

**Audra Wallace:** So it could be this answer and this answer and this answer to go down that path.

**Audra Wallace:** Informed submissions.

**Audra Wallace:** It's viewable only with one condition.

**Evangelina Sorello:** Yeah.

**Evangelina Sorello:** Okay, understood.

**Evangelina Sorello:** Thank you.

**Audra Wallace:** Some reason.

**Audra Wallace:** What have I messed up?

**Audra Wallace:** It's telling me I've got an error.

**Audra Wallace:** Okay.

**Audra Wallace:** Not sure.

**Audra Wallace:** Well, let me come over here so that you can see if I am in this and I want.

**Audra Wallace:** So here's actually that's not conditional field.

**Audra Wallace:** Okay.

**Audra Wallace:** So I'm going to make this one visible only if are you taking your medications is directed is yes.

**Audra Wallace:** Then I want to ask more questions about that.

**Audra Wallace:** So then when I come over and I can always view my form to see what it's going to look like for the patient by clicking View form page and when I do that I can see what the patient is going to see.

**Audra Wallace:** The asterisks tell me that these have to be selected.

**Audra Wallace:** And then when I press continue it goes to step two.

**Audra Wallace:** So that's where the two steps are in.

**Audra Wallace:** It's a different form.

**Audra Wallace:** And then here.

**Audra Wallace:** Are you taking your medications as directly?

**Audra Wallace:** If I click no, nothing happens.

**Audra Wallace:** If I click yes, it opens up the additional field that I had hidden and it could have opened if I said no, if that's what I had selected, it's not only yes, exactly, And then I'm able to submit and the patient sees.

**Audra Wallace:** Thank you.

**Audra Wallace:** When I go back over here, I can view submissions and you can see I just submitted it and when I submitted it.

**Audra Wallace:** And then I can view this submission and I can see my answers.

**Audra Wallace:** Now these are all blue and happy.

**Audra Wallace:** Right now when I create the contact fields, I can select what answer is concerning and then that answer would have showed up in red here instead.

**Audra Wallace:** So if I'm in do you have a fever during field type?

**Audra Wallace:** If I had said, do you have a fever?

**Audra Wallace:** If they answer yes, tell me.

**Audra Wallace:** That's alarming.

**Audra Wallace:** Then whenever I come in here, When I select yes.

**Audra Wallace:** And I view this submission.

**Audra Wallace:** Oh, shoot, I didn't update it on the form.

**Audra Wallace:** Whenever you change a contact field, you have to go into the form and remove that field and re add that field.

**Audra Wallace:** To update it.

**Audra Wallace:** Just a UI situation that I have brought up that will be changing in the future.

**Audra Wallace:** But right now, in order to update it on a form, you have to remove the field and re add it and then save it.

**Audra Wallace:** So.

**Audra Wallace:** Now if I submit this, it should show.

**Marcos Briceno:** Oh,.

**Audra Wallace:** And red.

**Evangelina Sorello:** Great.

**Evangelina Sorello:** Do you think you can share some of these questionnaires with our team or organization so we can, you know, had something for it to.

**Evangelina Sorello:** When creating the docs?

**Evangelina Sorello:** We had something that is.

**Evangelina Sorello:** Yes.

**Audra Wallace:** Yeah.

**Audra Wallace:** So I have on my list that I need to create some care plans, some workflows.

**Audra Wallace:** I'll add forms and contact cards that I'll.

**Audra Wallace:** Or contact fields so that y' all can see all of them.

**Evangelina Sorello:** Great, thank you.

**Audra Wallace:** Absolutely.

**Audra Wallace:** I think one of the other things.

**Evangelina Sorello:** We'll make sure it's on these notes that you were saying.

**Audra Wallace:** Yeah, yeah.

**Audra Wallace:** I think I showed you how to create a contact last time.

**Marcos Briceno:** Yeah.

**Audra Wallace:** And then.

**Audra Wallace:** Sorry.

**Marcos Briceno:** Yeah, no, you did.

**Audra Wallace:** Okay.

**Audra Wallace:** And then that's forms.

**Audra Wallace:** And then I think the other is potentially another big one is under messaging, creating message templates.

**Evangelina Sorello:** You were saying tasks.

**Evangelina Sorello:** I don't remember.

**Evangelina Sorello:** We know how to create tasks or broadcasting as well.

**Marcos Briceno:** Yeah, Actually, I was gonna say if we go over like tasks and broadcast, since this should be like the first thing, it'll be great because this way you can start creating content for those.

**Audra Wallace:** Already so under tasks in the upper right corner, you can press a new task and you can title it and then create the description.

**Audra Wallace:** And then there's all these different options of where you want it to start at.

**Audra Wallace:** So typically it would be requested here, priority.

**Audra Wallace:** It can be any of these.

**Audra Wallace:** You pick a due date.

**Evangelina Sorello:** One question here.

**Evangelina Sorello:** Do these statuses trigger something?

**Audra Wallace:** Yes, so they can.

**Audra Wallace:** Usually tasks are actually created primarily through the workflow.

**Audra Wallace:** So they would.

**Audra Wallace:** The workflow would create a task, and in the workflow, you can tell it how exactly to create the task.

**Audra Wallace:** And it would start in the requested status, because then whenever I come in to start work on a task, I can change it to in progress and that can trigger additional things or move it through the care plan eventually.

**Audra Wallace:** Or if I complete it, then it removes it off my list so that it's not an active task.

**Audra Wallace:** And that triggers things in the workflow as well.

**Audra Wallace:** And I select who benefits from the task and select the patient's name and who I want to perform it.

**Evangelina Sorello:** Performance and patients are preloaded through contacts.

**Audra Wallace:** Yes, those options are in the contacts.

**Audra Wallace:** Yep.

**Audra Wallace:** And then you can see the information here.

**Audra Wallace:** So this is primarily what people are doing, is coming in, seeing their task, and then being able to click on it and see whatever resources or additional tasks or comment on it.

**Audra Wallace:** Like I said, these are typically being created in the workflow rather than manually by individuals.

**Audra Wallace:** And in the workflow, we can go ahead and attach the resource or add subtasks if needed.

**Audra Wallace:** But when I come in to perform my task, I can come in here.

**Audra Wallace:** I can still attach a resource through here, and I can come in and attach this form submission that I just did, and then I can say that.

**Audra Wallace:** And add additional subtasks.

**Audra Wallace:** Maybe I want Maddie to.

**Audra Wallace:** You're not in here.

**Audra Wallace:** Maybe I want Mitch to do this subtask for me so that when I come back into my tasks, Mitch can see that his subtask is to check the pain.

**Audra Wallace:** I'm not sure why that resource did not save, but the resource would be right here and he'd be able to see it on the resource right there of who and what he needed to do.

**Evangelina Sorello:** So the resource could be one of those submitted forms, for instance.

**Evangelina Sorello:** Yeah.

**Evangelina Sorello:** So in the workflow you say, okay, this person mark that she or he has a fever.

**Evangelina Sorello:** So now the workflow creates this task.

**Audra Wallace:** And attaches the resource where they answered that concerning thing to the resource and then says, which patient submitted it right here and who it's supposed to be for.

**Audra Wallace:** And that might be a high priority.

**Audra Wallace:** You know, it Might be a stat if it's something that needs to be done right away.

**Audra Wallace:** And then I can come in here and say, like, tried calling three times.

**Audra Wallace:** You know, it's in progress.

**Audra Wallace:** And I can leave a note that says, like, Maryland wants this.

**Audra Wallace:** Try calling patient.

**Audra Wallace:** And I'm gonna leave it as a high priority because it still needs to be addressed.

**Audra Wallace:** But there's at least a log of what I've done and how I've done it.

**Audra Wallace:** Yes, Queen.

**Queendoline Akpan:** Okay, so if you create a subtraction, assign it to somebody, do they get a notification, like email, or they have to come to their dashboard and then see.

**Queendoline Akpan:** Or they've been assigned a subtask, how they fit?

**Audra Wallace:** Yeah.

**Audra Wallace:** So right now I believe, well, everything that's happened over there.

**Audra Wallace:** But the primary way they would find out is they would come onto their dashboard and see it.

**Audra Wallace:** We do have some workflows created to where the workflow is task creation.

**Audra Wallace:** And so then it sends a notification to Mitch that a task was created.

**Audra Wallace:** But it is not automatically.

**Audra Wallace:** That's not a smart role.

**Audra Wallace:** That's automatically in our system.

**Audra Wallace:** That would be something.

**Audra Wallace:** If you want to be notified when your task is created, you can create a subflow for that.

**Heitor Tessaro:** And why do you have like three my tasks on your sidebar?

**Audra Wallace:** So this is our dev account, and they are updating some of the tasks right now, the way that we create tasks.

**Audra Wallace:** And whenever they push it to production in this dev account, it duplicated instead of rewrote over the top of it.

**Audra Wallace:** So in a patient and in a client account, it would not have three tasks.

**Heitor Tessaro:** Okay, so you who has like home, my desks and care plans, that's it, right?

**Audra Wallace:** Yes.

**Audra Wallace:** So in a real one, it would be home, my tasks and care plans.

**Audra Wallace:** And I can switch.

**Audra Wallace:** Like, this one doesn't have any.

**Audra Wallace:** But you see, this is what it looks like for a client.

**Audra Wallace:** So it's.

**Audra Wallace:** And even right now, me going in and out, some of them are getting cleaned up.

**Audra Wallace:** So thanks for the question.

**Audra Wallace:** Sorry for the confusion with that.

**Audra Wallace:** Our dev account is very active and not always the most accurate.

**Heitor Tessaro:** Okay,.

**Audra Wallace:** And then you all said broadcasts, right?

**Audra Wallace:** So if I come into contacts.

**Audra Wallace:** Sorry, if I come into messaging and come into SMS broadcast to create a new broadcast, before I create a broadcast, I need to have a segment to send the broadcast to.

**Audra Wallace:** So that's why segments are important.

**Audra Wallace:** So we've talked about creating the segments.

**Audra Wallace:** But to create a new broadcast, you create the name.

**Audra Wallace:** You decide what segments to send it to.

**Audra Wallace:** You can send it to multiple if you want, up to three different Segments at a time.

**Audra Wallace:** It tells you who the selected segments are and how many contacts are in each.

**Audra Wallace:** And then you create a message.

**Audra Wallace:** In this message, I can type in, I can attach files, forms, courses, meeting links.

**Audra Wallace:** I can attach all the different resources that are being hosted within subflow.

**Audra Wallace:** Or I can use a templated message.

**Audra Wallace:** So we have people using broadcast of, they send it to all their managers to approve timesheets every two weeks for billing.

**Audra Wallace:** So they have a pre saved message template that I can show you how to create in a second that they're able to select from.

**Audra Wallace:** So that they can just select that and the message automatically loads.

**Audra Wallace:** They can then edit it if they want or personalize it or whatnot.

**Audra Wallace:** They come in and save.

**Audra Wallace:** I'm gonna actually take off Nashville phones because I think high paying is just me.

**Audra Wallace:** Actually before I do that, let me make sure that I'm not gonna.

**Audra Wallace:** Well, I'll just not actually send it.

**Audra Wallace:** So I create the broadcast.

**Audra Wallace:** Once I've created it, it gives you the information about what's going to happen.

**Audra Wallace:** Then you still need to send it or schedule send.

**Audra Wallace:** When it's in this draft phase right here, you can still go back in and edit it.

**Audra Wallace:** But once it has either been scheduled to send or sent, you cannot edit the broadcast.

**Audra Wallace:** So only while it's in this sort of draft phase here, then I can either press send broadcast and it sends the messages right away or I can schedule it for a later time.

**Audra Wallace:** So our clients usually for these regularly repeated messages that they're sending out, they'll come in at the beginning of the month or the beginning of the quarter.

**Audra Wallace:** They'll come in and they'll create all of them and have them schedule sent for specific days so that they know they're going to get sent out in the future.

**Audra Wallace:** Because then you schedule the broadcast and when I come into broadcast, I can see this is scheduled.

**Heitor Tessaro:** One question regarding.

**Heitor Tessaro:** Regarding the segment that it is using.

**Heitor Tessaro:** If you schedule for example to send the broadcast next month, is it going to consider the segment, the list that exists today on the segment, or the list that.

**Heitor Tessaro:** That exists on the segment next month?

**Heitor Tessaro:** Because they.

**Audra Wallace:** Because it's active.

**Audra Wallace:** That's a great question.

**Audra Wallace:** I should check with our team because I don't know the answer.

**Heitor Tessaro:** Okay.

**Audra Wallace:** Okay.

**Heitor Tessaro:** Another one is regarding.

**Heitor Tessaro:** Because from your demo it seems that this is a manual process.

**Heitor Tessaro:** Is there a way for you to automate these with the, with the flows, with the workflows?

**Heitor Tessaro:** Like to make it automatic in any.

**Audra Wallace:** Way or to use to create a broadcast from workflows?

**Heitor Tessaro:** I don't know if that makes sense, you know, or if it is better to just send a message directly to the patient when they reach like a certain position or certain stage on the flow, you know?

**Heitor Tessaro:** Yeah, I was just thinking that, I don't know, you are mentioning about.

**Heitor Tessaro:** You are mentioning that your clients are doing these once a month.

**Heitor Tessaro:** And I was thinking, why then?

**Audra Wallace:** Why are they not being created?

**Audra Wallace:** Yeah, that's a great question.

**Audra Wallace:** I think these still have to be manually created like this.

**Audra Wallace:** I did just ask them to make this duplicate, like being able to be duplicated, so that I can come in and duplicate it to the same thing and just change the date.

**Audra Wallace:** But that is not.

**Audra Wallace:** We don't have that yet.

**Audra Wallace:** So right now it's just to manually create broadcasts.

**Heitor Tessaro:** Okay.

**Audra Wallace:** Yeah, but you can see it scheduled, how many recipients it's going to, all that sort of thing.

**Audra Wallace:** And then from here you can cancel or archive the broadcast.

**Audra Wallace:** Okay, so about to create some changes to the UI here to be able to see the message and be able to potentially edit it and that sort of thing.

**Audra Wallace:** And your question about the.

**Audra Wallace:** If it's sending it to the current segment, the current contacts in the segment, or when it's active, when it sends.

**Audra Wallace:** I'll have to ask.

**Audra Wallace:** I think it's current, but it should probably be when it's active.

**Audra Wallace:** Yeah.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** If you reschedule a broadcast, what happens if you cancel?

**Heitor Tessaro:** Like, of course it's not going to center.

**Heitor Tessaro:** Okay.

**Audra Wallace:** If I come in and this is scheduled to send this Saturday.

**Audra Wallace:** If I come in here and I cancel it, then over here it shows it's canceled so that you still have all the details and there's a record it had been scheduled and then now it was canceled.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** So if you archive.

**Heitor Tessaro:** So the, the.

**Heitor Tessaro:** The data is removed.

**Audra Wallace:** If I archive it, it puts it over here.

**Audra Wallace:** So it's off of my primary list, but there is still record of it, and you can always restore it back to be able to have active record of it.

**Audra Wallace:** But it just keeps sort of the forever log, so it doesn't.

**Audra Wallace:** You don't permanently delete it.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** So like the main reason is just to clean up the.

**Queendoline Akpan:** This.

**Heitor Tessaro:** This page.

**Audra Wallace:** Yeah.

**Heitor Tessaro:** Okay.

**Heitor Tessaro:** Okay.

**Audra Wallace:** Yeah.

**Heitor Tessaro:** The other thing, when you are creating the broadcast to.

**Heitor Tessaro:** To personalize the.

**Heitor Tessaro:** The message, you can use any of the fields that are available on the profile.

**Heitor Tessaro:** Is that correct?

**Heitor Tessaro:** Or you can like add.

**Audra Wallace:** Yeah.

**Audra Wallace:** You can use any of the contact properties.

**Heitor Tessaro:** Mm.

**Audra Wallace:** And then you can use the different pieces of information, the different fields that you have gotten from the forms.

**Heitor Tessaro:** You also have access to the information that you receive from any form that the patient.

**Queendoline Akpan:** Okay, yes,.

**Audra Wallace:** They're all here.

**Evangelina Sorello:** One quick question is that, does these broadcasts only work for sms?

**Audra Wallace:** Yes, right now we only have the SMS broadcast the email.

**Audra Wallace:** They you can create a separate one for email.

**Audra Wallace:** So for email you do a new campaign and then similar process to write your email.

**Heitor Tessaro:** The difference that when you are creating an email campaign, you need to create these visual things, the actual email.

**Audra Wallace:** So one of the biggest things that they are using in the email campaign, the email campaigns is see if this is going to show you, yeah, you can see exactly what was sent right there.

**Audra Wallace:** So instead of writing and typing out a message, you create the email and that is done from this view.

**Audra Wallace:** One of the big things we're using in SMS broadcast is the pre done message templates.

**Audra Wallace:** So if you come into message templates, you can create a new message template and you title it, Sorry, I have a broken finger and I cannot type.

**Audra Wallace:** Well, so don't judge.

**Evangelina Sorello:** But yeah, don't worry,.

**Audra Wallace:** I can say hi.

**Audra Wallace:** And from there you can personalize it, you can add tags so that it's easily searchable and you save it.

**Audra Wallace:** And here it is right there.

**Audra Wallace:** So this can be sent directly in conversations, it can be used for broadcasts, it can be used in workflows.

**Audra Wallace:** So these pre built templates are a big foundation of what our clients are also using.

**Audra Wallace:** You can do this for text messages or emails.

**Audra Wallace:** So there's a couple of pre done ones, but what they typically are doing is coming in here for a new email template.

**Audra Wallace:** And then it saved too soon.

**Audra Wallace:** Well.

**Audra Wallace:** So you can drag and drop and create your email here.

**Audra Wallace:** So a lot of times we're sending out like the logo of the place, type it in and then you know, submit the link here and when you press save you're then able to use this template.

**Audra Wallace:** And when I do that, I see it here.

**Audra Wallace:** I say yep, that all looks exactly like I want it to.

**Audra Wallace:** I go to next step.

**Audra Wallace:** I can either add this at a specific contact to this or I can.

**Audra Wallace:** Or I can add it a whole segment so I can broadcast it from here.

**Audra Wallace:** So I would select who I want this to go to.

**Audra Wallace:** I press next step, I create the internal name, then the subject that the client is going to see and I can send now or schedule for later so they are able to determine that.

**Audra Wallace:** And then press send and then you confirm that you want to send it.

**Audra Wallace:** Now when that's done over on the email campaign you can see exactly what was sent or this is where you would see if it Was scheduled to be sent as well.

**Audra Wallace:** Oh, I'm so sorry.

**Audra Wallace:** I didn't see your hand up.

**Audra Wallace:** You just gotta interrupt me.

**Audra Wallace:** I get.

**Evangelina Sorello:** No, it's okay.

**Evangelina Sorello:** Because it was also what we needed to learn what you were saying.

**Evangelina Sorello:** So it's okay.

**Evangelina Sorello:** My question was about.

**Evangelina Sorello:** You said that you could use these messages templates in conversations, and I was wondering where or when these conversations happen.

**Audra Wallace:** So the two way texting is a big piece of communication in our platform.

**Audra Wallace:** So being able to in the workflow send a message.

**Audra Wallace:** Then if the patient has a question or wants to respond and confirm something, they're able to text right back when they text back.

**Evangelina Sorello:** With a message.

**Evangelina Sorello:** With an sms.

**Audra Wallace:** Message with an sms.

**Audra Wallace:** Okay, so the workflow, you can see the workflow said that I have not submitted their intake form.

**Audra Wallace:** Right.

**Audra Wallace:** It comes to my phone and as the patient, I get the text message from subflow just like a normal text.

**Audra Wallace:** And then I can say, you know, if it was a form submission or if it was asking a question or sending information, the patient can text back just like they would text anything else.

**Audra Wallace:** And it could.

**Audra Wallace:** And it comes up with a blue circle around it with a blue dot.

**Audra Wallace:** And you can see here I have an unread message and it shows that the patient texted back.

**Evangelina Sorello:** So it's not that they have to access a portal and then go to a specific section and from their reply messages.

**Evangelina Sorello:** No, correct.

**Audra Wallace:** They go straight back from the text message.

**Audra Wallace:** So that's part of the ease of access, is it comes to them.

**Audra Wallace:** Typically, the workflow is sending messages, straight text messages.

**Audra Wallace:** You can see in here.

**Audra Wallace:** You can see exactly.

**Audra Wallace:** This automated message was from one of the workflows telling me to fill out this form.

**Audra Wallace:** So on my computer, I can click this and go specifically to this form and fill out the form.

**Audra Wallace:** And I never had to submit or I had to go into a portal or do anything else.

**Audra Wallace:** But if I.

**Audra Wallace:** If as the patient, I have a question specifically about this and say, like, hey, I just answered this information, But I also have another question.

**Audra Wallace:** They could text back immediately.

**Audra Wallace:** From a record standpoint in subflow, you can see this was an automated message, meaning it's from the workflow versus Joshua was in here working one time and texted me or this one.

**Audra Wallace:** This is what I just sent.

**Audra Wallace:** I'm logged in and sent a message.

**Audra Wallace:** And you can see the patient, also me.

**Audra Wallace:** So it's a little confusing.

**Audra Wallace:** But the patient just texted back over here.

**Evangelina Sorello:** Yeah, yeah.

**Evangelina Sorello:** So there is no patient portal.

**Audra Wallace:** Yeah, perfect.

**Evangelina Sorello:** That was one of my questions.

**Evangelina Sorello:** And it's great that they didn't just reply a message.

**Evangelina Sorello:** Honestly, I didn't know that they can.

**Audra Wallace:** Reply it right back.

**Audra Wallace:** But this is another place where they can use the templates.

**Audra Wallace:** So if I am in here and she says I want to know more, I can come in and it has all the extra information here and then I can just edit it and say, you know, for you also do this.

**Audra Wallace:** Okay.

**Audra Wallace:** And then it sends.

**Evangelina Sorello:** Great, great.

**Evangelina Sorello:** Thank you.

**Evangelina Sorello:** For now we won't be able to test this because we don't have like.

**Audra Wallace:** The U.S. yeah, but they're working on that looking.

**Audra Wallace:** But if you're ever in here and want to send me messages and see how you attach it and how you work on templates, feel free to type something.

**Audra Wallace:** If you're on the platform, you can send the message and then it'll go to me and then I can respond back.

**Audra Wallace:** So you can see sort of how that goes.

**Evangelina Sorello:** Yes.

**Evangelina Sorello:** Maybe we need a screenshot or something.

**Evangelina Sorello:** Yeah, that would be very helpful.

**Evangelina Sorello:** Thank you.

**Audra Wallace:** Absolutely.

**Audra Wallace:** Feel free to use me.

**Audra Wallace:** Okay.

**Audra Wallace:** Just realized that we are over time again.

**Audra Wallace:** What else could be helpful for today?

**Audra Wallace:** And then do we also need to schedule another follow up?

**Heitor Tessaro:** I think that.

**Heitor Tessaro:** Go ahead.

**Marcos Briceno:** No, I just.

**Marcos Briceno:** I think that's to create like initial drafts for this test that maybe will be enough like I imagine like how to create tasks, how to create a segment, how to create a broadcast and a broadcast and message template, which I think are all correlated.

**Marcos Briceno:** Right.

**Marcos Briceno:** I think we can definitely create some drafts on those and maybe send them to you for review and see what you think.

**Marcos Briceno:** And then maybe we can set up already a meeting then we can go over it and say can give us your feedback.

**Audra Wallace:** That sounds great.

**Marcos Briceno:** Yeah, we just.

**Marcos Briceno:** But that.

**Marcos Briceno:** Actually I'll ask Mitch because we haven't decided like on framework for the documentation, but we can see that with him directly and we.

**Marcos Briceno:** Anyways we can still create those templates.

**Marcos Briceno:** Yeah, the drop.

**Marcos Briceno:** Sorry.

**Marcos Briceno:** Yeah, I think that for now maybe I don't know it or if you think we could go over something else or.

**Heitor Tessaro:** No, no, not today.

**Heitor Tessaro:** But I was talking with Marcus before this meeting that maybe it would be useful like after we address these main topics for us to have like an overview about day to day usage.

**Heitor Tessaro:** Like to understand the flow and like not necessarily going deeply on each of these features, but to understand like, okay, this is how the user is actually using every day, you know, so that is all really useful.

**Heitor Tessaro:** And another approach is okay, if you are starting.

**Heitor Tessaro:** Start using the platform.

**Heitor Tessaro:** These are the steps to setting everything, you know, the basic.

**Heitor Tessaro:** So these two approaches could be useful for us.

**Heitor Tessaro:** But first we can address the main topics and then we can go ahead and discuss this, you know, because this usually defines the documentation structured, you know.

**Heitor Tessaro:** Yeah, but these the guys that the specific guides are useful for you to share with the client.

**Heitor Tessaro:** But for someone that is accessing the documentation for the first time, having like an overview about the process.

**Audra Wallace:** Yeah, that makes a lot of sense.

**Marcos Briceno:** And another thing is I also like going back to something that Vanja said I think will be cool, but I think we can do this as we go.

**Marcos Briceno:** No need to like set up space that we create like a glossary and define like the terms like that we're going to use across documentation just so that we are consistent with it.

**Marcos Briceno:** I'll think of a way that we can do it interactive.

**Marcos Briceno:** Maybe like in a canvas in Slack.

**Marcos Briceno:** We can have one and like put the terms there and save them there and then we can export that for ourselves.

**Marcos Briceno:** Because I think that especially for like end user documentation, it's important that we always use the same name for things like for example, is this call a module?

**Marcos Briceno:** Are we going to say like oh, this is the messaging module or is this the dashboard module?

**Marcos Briceno:** Are we going to call it always like that?

**Marcos Briceno:** Or it has another name or something.

**Audra Wallace:** That's a great point.

**Audra Wallace:** And I think some of that I'll have to run by Mitch and Will because I think of course we also see how we're calling it.

**Marcos Briceno:** Because we faced so some issues with that before that we also like.

**Marcos Briceno:** Okay, so but this is called like this.

**Marcos Briceno:** But sometimes other people in the company also call it another name, you know, so it goes over different.

**Marcos Briceno:** But yeah, we can do that as we go, it's no problem.

**Heitor Tessaro:** And we send it to you.

**Heitor Tessaro:** That sounds great, Mark.

**Heitor Tessaro:** Just to finish, should we already schedule a meeting or should we try to create the content first?

**Marcos Briceno:** I think we can.

**Marcos Briceno:** Maybe you can schedule a meeting but like by the end of the week, like this week?

**Marcos Briceno:** I don't know.

**Marcos Briceno:** This way we can like do the drafts during the week and then present it to you guys on.

**Marcos Briceno:** On Friday we'll send it, try to send it before to you.

**Marcos Briceno:** But what do you think?

**Marcos Briceno:** You think it's a good idea?

**Heitor Tessaro:** It's a good idea.

**Heitor Tessaro:** When should we try to schedule?

**Heitor Tessaro:** I don't know.

**Heitor Tessaro:** Audra, when are you available?

**Audra Wallace:** I think to Friday.

**Audra Wallace:** Friday morning.

**Audra Wallace:** I'm free pretty much all morning.

**Audra Wallace:** I am really bad at time zones, so I don't remember what right now.

**Audra Wallace:** 11:37 For me.

**Marcos Briceno:** Yeah, you're two hours before us.

**Marcos Briceno:** So how early.

**Audra Wallace:** Can y' all do it?

**Marcos Briceno:** Yeah, I think.

**Marcos Briceno:** Do you think the same time as today or maybe 12 here?

**Marcos Briceno:** I don't know.

**Audra Wallace:** Yeah.

**Heitor Tessaro:** Or yeah.

**Heitor Tessaro:** Yeah, for me it's okay.

**Heitor Tessaro:** But if Audra wants to do it earlier for me, it's okay as well.

**Marcos Briceno:** No problem.

**Heitor Tessaro:** I don't know how do you want.

**Marcos Briceno:** Can you do it?

**Heitor Tessaro:** Will be.

**Marcos Briceno:** 9:30 For you in the morning.

**Marcos Briceno:** That'll be 11:30 for us later.

**Marcos Briceno:** Okay.

**Marcos Briceno:** A good one.

**Heitor Tessaro:** Yeah.

**Marcos Briceno:** Okay.

**Heitor Tessaro:** Perfect.

**Queendoline Akpan:** Perfect.

**Heitor Tessaro:** Okay, awesome.

**Audra Wallace:** Thank you all so much.

**Audra Wallace:** I appreciate it.

**Audra Wallace:** You mind sending that over?

**Marcos Briceno:** Oh, sorry.

**Audra Wallace:** We all send the schedule, the meeting invite over.

**Marcos Briceno:** Yeah, yeah, do that.

**Marcos Briceno:** No worries.

**Audra Wallace:** Sounds great.

**Audra Wallace:** Thank you all so much.

**Marcos Briceno:** Thank you.

**Marcos Briceno:** Thank you.

**Audra Wallace:** Have a birthday, a great day.

**Evangelina Sorello:** Bye.

**Audra Wallace:** Bye.

**Audra Wallace:** Bye.

**Marcos Briceno:** Bye.
