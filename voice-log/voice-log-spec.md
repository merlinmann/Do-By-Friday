# A Quickie Voice Log Spec

By Merlin Mann  
for [_Do By Friday_](https://dobyfriday.com "A weekly challenge show hosted by Alex Cox and Merlin Mann")

## Short Version

By invoking a quick phrase, Siri captures a sentence or two of dictated text and adds it to a bucket where the user can do something with it later. Critically, it also captures the location where the note was made as well as the date and time of the note. The note is written to a file in a format and file-kind that's suitable for other uses.

## Genesis

I'm new to riding a ±70 lb. ebike on which balance can be tricky at best and where ~20mph speeds mean I _really_ prefer to keep both hands on the handlebars and always ready to hit the brakes. I don't even like using one hand to adjust a mirror or signal a turn—let alone trying to fiddle with a device like my Apple Watch or iPhone.

But, when I'm riding my bike, I often find myself wanting to capture a short note via Siri. Originally, I just craved a way to capture something about a given route, especially when I want to remember that a stretch of road is particularly rough or has bad traffic, etc.

## But, Also

As with so many activities that are _not work_ (among which I'd also count taking a shower or urinating), I've found my bike rides are often when I have thoughts or ideas that I'd like to return to later. Whether it's remembering I need to buy toilet paper or having a left-field idea for a podcast topic, it'd be handy to have a way to capture a short note about pretty much anything.

With that said, I can think of _so_ many other uses for a simple voice log that I'd personally utilize all the time. I can envision a general purpose _inbox_ in the truest sense of the word; unprocessed thoughts of any sort that may be useful to return to and process later—but, which require the absolute minimum of vocal effort to capture. Fast is good.

## Some Options I've Considered

* **Apple Reminders**. "Hey, Dingus, remind me to [_do a thing_] in one hour" is something I yell into the air a lot, and it usually works a treat. But, even more important than not wanting to dilute my TODO list by adding things that aren't tasks, to my knowledge, Reminders does not natively capture stuff like the _time_ that the Reminder was created or the geolocation data for _where_ it was created.
* **Apple Notes**. Yes: using Siri to append to an Apple Note seems like table stakes for such an app and service. But—at least to my knowledge—appending to a Note is not possible using Siri (at least in the absence of something like a Siri Shortcut that I lack the skills to make)
* **Drafts**. This is another very promising contender, especially since Drafts Actions like [WalkWriter](https://actions.getdrafts.com/a/1Mw), [Quick Journal](https://actions.getdrafts.com/g/1Sd), or [Assemble Diary](https://actions.getdrafts.com/a/1P8) seem this 🤏 close to doing what I want. I just haven't figured out how to do it via Siri and in an output format I'd like.
* **Day One, Diarly, or similar**. Obviously it makes sense to start with a diary app/service since _logging_ is definitionally what they do. But, in my admittedly short time looking into it, I haven't found a way to make it all happen hands-free. Also, nobody likes subscribing to a service before knowing whether it'll do exactly what they need.
* **Apple Shortcuts**. While my intuition tells me this can likely be done via one Shortcut, I haven't found one that does exactly what I'm looking for, and I lack either the skills or inclination to make it from scratch myself.

## How It Should Work

1. **Hail via Siri with a short and unambiguous phrase**
    * none of this "Hey, Dingus, append a note to Merlin's cycling journal for today…"-type stuff
    * should work equally well on Apple Watch and iPhone
    * hailing phrase should be user-customizable.
      * Personally, I'll want mine to be _crazy_ short with hard consonants that my iPhone can hear and understand amidst the wind and traffic of a bike ride.
        * EG
            * "Hey, Siri, tack this…"
            * "Hey, Siri, real quick…"
2. **Capture 1-2 dictated sentences**
    * Successfully accepting something longer is fine, but just in my own usage, I won't be dictating a novel.
         * Also, it'd be valuable not to have to look down and see whether Siri "got it."
    * My own typical notes might be stuff like:
        * "40th between Judah and Kirkham has lots of holes"
        * "Google the new coffee place near Kezar"
        * "Get my right brake looked at"
        * "Don't do Great Highway on windy days"
3. **Include location and time metadata**
    * At a minimum, I want to capture:
        1. **location** as a [US street address](https://desktop.arcgis.com/en/arcmap/latest/manage-data/geocoding/what-is-an-address.htm)
            * also capturing lat/long alongside the address would be great
              * but having the component parts of the address written out as "fields" is very desirable
        2. **date and time** the note was created
    * Other easy/popular metadata like current weather would be cool, but is not required
4. **Generate a useful and functional log file**
    * Results should be portable and easy to do…other stuff with.
    * Viz. I'll definitely often want to _do_ something with the log, like generate a map or make a spreadsheet, so I need the results to be formatted into fields or similar.
    * I'd also prefer not to _just_ have separate lines with carriage returns in a text file.
         * So, if you need to choose between this being "pretty to look at" vs. "functionally useful," please pursue the latter.
    * Suggestions that spring to mind include
        * `CSV`
        * `JSON`

## Do Not Want

* No extra work to perform before or after capture
    * I don't want to have to make a new document or list each time I use it
    * I don't want to just end up with a bunch of separate text files generated per note.
    * I don't want to have to _assemble_ the results later on
* No exotic formats
    * While I'm _potentially_ open to using third-party apps and services, I'd love for this to be doable with stock Apple, free-as-in-beer software.
    * Thus, to make this most broadly useful to the community, please prefer open or Apple-native formats over paid or proprietary options.
        * No one should need an Office 365 license to recall where a clean public restroom exists.
* TKTKTK

## Nice to Haves

* Tags
    * I have _no idea_ how to do this, but it'd be neat if the inclusion of a given word in the natural dictated text could cause the entry to be tagged with one of _n_ predefined keywords.
* TKTKTK

----
