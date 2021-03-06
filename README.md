# SNEAKEZAPP
# EXAMPLE GROUP PROJECT README

# TUNIN

## Table of Contents
Unit 8: Group Milestone - README Example
===

:::

# TUNIN

## Table of Contents
1. [Overview](#Sneakez App)
1. [Product Spec](Pages within App)
1. [Wireframes](#Wireframes)

## Overview
### Description
Allows users to share collectoin and reach out to people that interenst in selling shoes at their current shoes event.
   - **Market:** Anyone that takes pictures could enjoy this app. Ability to follow and hashtag based on interests and categories allows users with unique interests to engage with relevant content.
   - **Habit:** Users can post throughout the day many times. Features like "Stories" encourage more candid posting as well. Users can explore endless pictures in any category imaginable whenever they want. Very habbit forming!

### App Evaluation
- **Category:** Social Networking / Music
- **Mobile:** This app would be primarily developed for mobile but would perhaps be just as viable on a computer, such as tinder or other similar apps. Functionality wouldn't be limited to mobile devices, however mobile version could potentially have more features.
- **Story:** Analyzes users music choices, and connects them to other users with similar choices. The user can then decide to message this person and befriend them if wanted.
- **Market:** Any individual could choose to use this app, and to keep it a safe environment, people would be organized into age groups.
- **Habit:** This app could be used as often or unoften as the user wanted depending on how deep their social life is, and what exactly they're looking for.
- **Scope:** First we would start with pairing people based on music taste, then perhaps this could evolve into a music sharing application as well to broaden its usage. Large potential for use with spotify, apple music, or other music streaming applications.

## Product Spec
### 1.News Page,Calendar,Map, Profile & Shoe Collector Page 



* User logs in to access previous chats and preference settings
* User picks what their favorite city. User will also be able to post the location of the shoe event. (Think 23Isback.com interface)
* Matches have a chat window to get to know each other, with the ability to skip user if they dont want to coneversate of dicate the objective of the confernce
* Profile pages for each user
* Settings (Accesibility, Notification, General, etc.)


### 2. Screen Archetypes

* Login 
* Register - User signs up or logs into their account
   * Upon Download/Reopening of the application, the user is prompted to log in to gain access to their profile information to be properly matched with another person. 
   * ...
* Messaging Screen - Chat for users to communicate (direct 1-on-1)
   * Upon selecting shoe evenet users matched and message screen opens.
* News Screen 
   * Allows user to upload a photo and fill in information that is interesting to them and others regarding current information
* .Loading Screen
   * Allows user to be able to choose their desired shoes, from nike, puma, rebok or Retro Jordan
* Settings Screen
   * Lets people change language, and app notification settings.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Front Ad
* Loading Screen
* 3 Kicks Start pages
* Calendar
* News
* Profile
* Map of Current Events
* Chat Room


**Flow Navigation** (Screen to Screen)
* Forced Log-in -> Account creation if no log in is available
* Customer will here a Starting tune
* Customer is will be to help of the resouces of knowing current events.
    ``
*![](https://i.imgur.com/WmTwj8L.jpg)

## Schema 
### Models
#### Post

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique id for the user post (default field) |
   | author        | Pointer to User| image author |
   | image         | File     | image that user posts |
   | caption       | String   | image caption by author |
   | commentsCount | Number   | number of comments that has been posted to an image |
   | likesCount    | Number   | number of likes for the post |
   | createdAt     | DateTime | date when post is created (default field) |
   | updatedAt     | DateTime | date when post is last updated (default field) |
### Networking
#### List of network requests by screen
   - Home Feed Screen
      - (Read/GET) Query all posts where user is author
         ```swift
         class DataController{
//   let persistentContainer = NSPersistentContainer(name: "LibraryDataModel")
//
//    var context: NSManagedObjectContext {
//        return self.persistentContainer.viewContext
//    }
//
//    func initalizeStack() {
//           // 2.
//           self.persistentContainer.loadPersistentStores { description, error in
//               // 3.
//               if let error = error {
//                   print("could not load store \(error.localizedDescription)")
//                   return
//               }
//
//               print("store loaded")
//           }
//       }
//
//    func createSneaker(name:String,brand:String,date:String){
//        let sneaker = SneakerData(context: context)
//        sneaker.name = name
//        sneaker.brand = brand
//        sneaker.date = date
//        self.context.insert(sneaker)
//        do{
//        try self.context.save()
//
//        }catch{
//            print("ERRROROR")
//        }
//    }
//
//    func fetchUsers() throws -> [SneakerData] {
//        let sneakers = try self.context.fetch(SneakerData.fetchRequest() as NSFetchRequest<SneakerData>)
//        return sneakers
//    }
         ```
      - (Create/POST) Create a new post in Chat
      - (Delete) Delete existing like
      - (Create/POST) Create a new comment on a post
      - (Delete) Delete existing comment
   - Create Post Screen
      - (Create/POST) Create a new post for shoe calendar events
   - Profile Screen
      - (Read/GET) Query logged in user object
      - (Update/PUT) Update user profile image
#### [OPTIONAL:] Existing API Endpoints
##### ' An API Of ShoeCollector'
- Base URL - [http://www.buildmyapp.com/api](http://www.buildmyapp.com/api)

   HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    | /characters | get all characters
    `GET`    | /characters/?name=name | return specific character by name
    `GET`    | /houses   | get all houses
    `GET`    | /houses/?name=name | return specific house by name

