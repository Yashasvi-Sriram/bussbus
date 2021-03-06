# bussbus

## description
- A simple tool for quickly glancing MetroTransit departures in Minneapolis/St. Paul.

## code
- This is a minimal android project in `Kotlin`.
- Uses MetroTransit public API <https://svc.metrotransit.org/nextrip>.

## documentation
- The documentation for the code is itself.

## usage
- The app is targetted towards people who use some metro transport stops frequently. For example, going to work, coming back home, going to grocery store...
- Find the app at [Play Store](https://play.google.com/store/apps/details?id=io.buggedbit.bussbus).
- Install the app on an android device.
- Add some stops (using respective stop ids) and give them (unique) names.
- The departures from those stops shall appear.
- Similarly remove stops when not needed.
- The departures are not automatically updated. A sync button on the bottom shows how long ago was the last sync. Press that button to sync again.
- No login required.
- No location permission needed.
- If a stop's departures can not be fetched, its id might be wrong. Try removing and adding it again.

## demonstration
| | |
| --- | --- |
| Adding a stop | ![](./github/add.gif) |
| Removing a stop | ![](./github/remove.gif) |
| Sync | ![](./github/sync.gif) |

### portrait mode
| Adding a stop | Removing a stop | Viewing departures |
| --- | --- | --- |
| ![](./github/add_portrait.jpg) | ![](./github/remove_portrait.jpg) | ![](./github/view_portrait.jpg) |

### landscape mode
- Adding a stop

![](./github/add_landscape.jpg)

- Removing a stop

![](./github/remove_landscape.jpg)

- Viewing departures

![](./github/view_landscape.jpg)

## roadmap
- [x] Scroll view in stop departures activity.
- [x] Display stop name before requesting departuresList. Useful in case of laggy response.
- [x] Update last sync state in sync() rather than in success callback. Safer choice in case of laggy response.
- [x] Adding a stop.
    - [x] Where can stop ids be found? - Link provided.
    - [x] StopId validation: len == 5 & uniqueness.
    - [x] StopName validation: 0 < name & uniqueness.
    - [x] Db add.
    - [x] finish() on add.
- [x] Read stops from db.
- [x] Updated list on add/remove finish() return.
- [x] Removing a stop.
    - [x] Recycler view.
    - [x] Db remove.
    - [x] finish() on remove.
- [x] Simplify Holder object.
- [x] Inline shared pref commit() & Error check shared pref commit()
- [x] Improve validation comments, Improve messages; add period at the end.
- [x] Remove background pictures if copyrighted.
- [x] Improve styling.
- [x] Decrease num of id references to xml elements.
- [x] Check internet connection.
- [x] Demo.
- [x] Improves validation message display in AddStopActivity. (Uses above keyboard Snackbars).
- [x] Limit stop nickname len.
- [x] Improve Layout rules in Stop Departures.
- [x] Update demos.
- [x] Release on play store.
- [ ] Simplify last sync x min ago periodic update.
- [ ] Check internet connection idiomatically.
