---
layout: project
type: project
image: img/Manoa.png
title: "Manoa Mentoring"
date: 2024-5-10
published: true
labels:
  - Java
  - Meteor React
  - Github
summary: "Manoa Mentoring, aims to bring together students and mentors."
---

<p align="center">
<img width="900px" class="img-fluid" src="../img/site.png">
</p>
<p align="center">
Landing Page
</p>

## [Manoa Mentoring](https://manoa-mentoring.site/)
Manoa Mentoring is a University of Hawaii centric application that allows students and mentors to organize, host, and promote tutoring sessions. It's a collaborative project we designed to provide an efficient method for students to engage in study sessions. Sessions can be created, joined, and edited to provided users customization and organization of sessions. We've also implemented a leveling system to promote users to engage in both hosting sessions and attending them. When setting up accounts, users have the option to set their major, location, and preference of session between Online, In-Person, or Both. 

[Source Code](https://github.com/manoa-mentoring)

[Project Page](https://manoa-mentoring.github.io/)

## My Role in the Process
There were 3 primary stages in the development of our project. They were broken down into 3 milestones. Across those three miletones some of my main contributions included:

Creating am administrative page that allowed moderation for users and sessions. 

Creating some of the data structures used across the site like the sessions structure which is frequently used. I included a snippet of the proptype declarations for the structure, very straightforward but also necesarry for the organization and maintenance down the line. I also ensured that it was properly published and functional.

~~~
StudySession.propTypes = {
  studySession: PropTypes.shape({
    name: PropTypes.string,
    subject: PropTypes.string,
    location: PropTypes.string,
    hostName: PropTypes.string,
    dateStart: PropTypes.instanceOf(Date),
    dateEnd: PropTypes.instanceOf(Date),
    image: PropTypes.string,
    description: PropTypes.string,
    owner: PropTypes.string,
    joinedUsers: PropTypes.arrayOf(PropTypes.string).isRequired,
    _id: PropTypes.string,
  }).isRequired,
  onDelete: PropTypes.func.isRequired, // Function to handle deletion
};
~~~

During out testing phases, I created the tests for the admin page, sign in, and sign up. As well as linking all of my peers tests together to ensure that the site passed everyone's individuals tests. These tests ensured that every function offered by the site worked and was recreatable regardless of credentials. Here's a snippet of the admin test.

~~~
class ListcontactsadminPage {
  constructor() {
    this.pageId = '#list-stuff-admin-nav';
    this.pageSelector = Selector(this.pageId);
  }

  /** Asserts that this page is currently displayed. */
  async isDisplayed(testController) {
    await testController.expect(this.pageSelector.exists).ok();
  }
}
~~~





