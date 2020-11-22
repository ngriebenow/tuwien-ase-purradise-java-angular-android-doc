
| Issue| #116 |
| ------ | ------ |
| Date | 2020-11-04 |
| Start | 10:00 |
| End | 11:00 |
| Attendees | G, L, M, N, S, T |

### Goals
- Discuss Sprint 2


Model Upload: We save the object file (.obj) and the png/jpeg file (.png/.jpeg) in our H2 database.
Maximum file size: 8MB.

Each time the customer opens the Recommendations, they see 5 recommendations. Backend just uses the filter function of the Filter feature, but instead only returns 5 animals.

Web: thumbs-up, thumbs-down
Android: swipe-right, swipe-left

Case no animals match the filter: Warning message that there are no animals available that fully match the preferences.

Possible Improvement for Sprint 3: add almost-matches from neighborhood


We do not allow transitions between user accounts. A customer is always a customer and canot transition to kepper or admin, etc.

We use Retrofit + RxJava.

Two possibilites in ARCore
- Instant view: if plane rendering takes longer, instantly place AR model into the 3D space
- Wait till plane is recognized by ARCore (default)
We will handle this issue in Sprint 3.


Sprint 2 terminates on 2020-12-08 23:59.

On Tuesday we decide whether we will need another Jour-fixe. Default: no jour-fixe.

As soon as MR is done by Nicolas, Thomas will branch dev to master and tag it with:  
Tag: v0.1