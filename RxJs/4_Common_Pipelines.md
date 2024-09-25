# Four RxJS pipelines
(https://www.youtube.com/watch?v=wQ8jXlWMoCo&t=170s)

## General approach

<ul>
  <li>Before choose needed pipelines, answer the questions first:
    <ol>
      <li>What do we have?</li>
      <li>What do we want?</li>
      <li>When do we want it?</li>
    </ol>
  </li>
  <li>To respond to an action - use **Subject**/**BehaviorSubject**.
  Whenever after some action occurs and this cause RxJS stream to do smth

   ![alt text](screenshots/image-7.png)<br>

  `Subject<string>()` - does not have initial value <br>
  `BehaviorSubject<string>('')` - always have initial value<br>
  When component subsribe to `enteredUser$` observable of `BehaviorSubject` - first it will have its default value(''). If it subsribed late after `Subject` have emitted several things - it will always give to subsribers - **last** emitted value.
  </li>
</ul>

## 1. Retrieve Related Data Pipeline (switchMap)
- **What do we have?** - Typed in search userName
- **What do we want?** - List of posts related to typed in user
- **When do we want it?** - Aby time the user changes typed in search field
![alt text](screenshots/image-8.png)<br>

### 1.1 Retrieve Related Data Pipeline (with error handling!)
- Retrieve related data pipeline with handling case whe user/post not found
![alt text](screenshots/image.png)<br>
![alt text](screenshots/image-1.png)<br>
Rewripe pipeline:<br>
![alt text](screenshots/image-2.png)<br>

## 2. Lookup Reference Property Pipeline (combineLatest)
To work with **multipe streams**, use a **combination** operator <br>
 1. Retrieve **category name** when initially we have only **categoryId**
- **What do we have?** - Post and PostCategory
- **What do we want?** - Add categoryName to the Post entity
- **When do we want it?** - Whenever we get the data
![alt text](screenshots/image-3.png)<br>
Lets break into smaller pieces with exemption handling<br>
![alt text](screenshots/image-4.png)<br>
How to reuse the Retrieved categories (since it will not change)
`shareReplay(1) - will cache the last emitted item`<br>
![alt text](screenshots/image-5.png)<br>
Rewrite pipeline to:<br>
![alt text](screenshots/image-9.png)<br>
The same pipeline splitted into methods:<br>
![alt text](screenshots/image-10.png)<br>

## 3. Grouping pipeline
- **What do we have?** - Posts
- **What do we want?** - Posts groped by category
- **When do we want it?** - Whenever the data is ready for the page
![alt text](screenshots/image-11.png)<br>
**concatAll**<br>
![alt text](screenshots/image-12.png)<br>
**groupBy**<br>
![alt text](screenshots/image-13.png)<br>
**mergeMap**<br>
![alt text](screenshots/image-14.png)<br>
**toArray** (to get array with all tuples and render it instead emitting by one value)<br>
![alt text](screenshots/image-15.png)<br>

## 4. Autocomplete pipeline
![alt text](screenshots/image-16.png)<br>
- **What do we have?** - List of categories
- **What do we want?** && **When do we want it?** <br>
Type: Filter the list<br>
Click: Open the list<br>
Focus: Open the list<br>
Click x: Clear and open the list<br>
For each action we will use own `Subject/BehaviorSubject`<br>

Event handlers<br>
![alt text](screenshots/image-18.png)<br>
Search func<br>
![alt text](screenshots/image-19.png)<br>
Merge all handlers in *operations$* stream<br>
![alt text](screenshots/image-20.png)<br>
Combine opeartions$ stream with categories to work with them together and return array of ategories whick includes types substring othetwise display whole list of categories<br>
![alt text](screenshots/image-21.png)<br>

