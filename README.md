# Beyond Adaptive Web Design

## Abstract

Mobile device penetration grows rapidly and it brings not only different display sizes with new human interaction methods, but also new kinds of internet connection. So it is neccessary to adapt web pages for different devices and new interaction methods. In our work, we follow ,,Mobile First'' and ,,Progressive Enhancement'' design, which emphasizes a great performance on mobile devices and later profit on classical desktop computers. We present a new way of web components adaptation based on a device features and external conditions in our work and new possibilities of interaction with web application based on speech recognition, motion or device rotation. The evaluation of the proposed method of adaptation shows slightly better results than original approach.

## Introduction

The Web is continually evolving and we need to evolve with it. It used to be easier to manage browsers when there were just a few of them on the desktop. Today we not only have to deal with a wide range of desktop browsers but mobile devices, tablets, televisions, weareable devices and more. Even for the average web site things have changed a lot over four years: browser share, operating systems, screen resolutions, and more [User Interface 17].

The basic approach how to provide an optimal viewing experience is to use Responsive web design which comes with fluid grids, flexible images and CSS3 media queries [Responsive Web Design].
While creating flexible layouts is important, there’s a whole lot more that goes into truly exceptional adaptive web experiences. The principles of Adaptive Design are: ubiquity, flexibility, performance, enhancement and future-friendliness [Beyond Squishy: The Principles of Adaptive Design].

The power of the web is its ubiquity. No one knows what the landscape is going to look like in a couple years, but there’s a good chance the new devices in a few years from now will have access to the web. Because of this, we need to preserve and embrace the web’s ubiquity. This requires us to deliver full web experiences regardless of how and where people access the web. 
It's important to continue creating flexible interfaces that can adapt to any screen size. Performance often takes a back seat to everything else. Progressive enhancement, feature detection and many other techniques allow us to build up a core experience that allow us to support more devices while still optimizing for the the best of the best. The key aspect of Future Friendly thinking is to acknowledge and embrace unpredictability. Nobody knows where things are going but the one thing we can count on is the evolution.

Adaptive web design is essentially progressive enhancement at its core, but it’s being applied to a much larger, more diverse landscape than when the term progressive enhancement was first coined. We now have Web-enabled smartphones, tablets, e-readers, netbooks, watches, TVs, phablets, notebooks, game consoles and more. We also have many types of internet connections with different qualities.

Responsive design is one technique in an adaptive web design strategy. Creating flexible layouts is extremely important, but it’s just one piece of the puzzle. It’s also important to consider a whole host of other factors as well: ergonomics, touch capability and other input methods, internet connection, geolocation and many other features that can be detected.

We consider “adaptive web design” as a synonym with creating a single Web experience that modifies based on the capabilities of the device and browser. Website can access superpowers in devices.

## Adaptive Input methods

As we have many types of devices with web access we also have to adapt input methods for them. It is not just about screen sizes, but many displays also have touch capabilities.

Web browsers on TVs are actually really good but the input is terrible so no one uses them. Input is much more important to interface design than screen size. The input defines what a design needs to do in order to accomplish a task [Adaptive Input].

We also have wearable computers. The current Google Glass interface is limited to a floating rectangle above head. We don’t have full range of motion and, as a result, no spatial cues or depth in the interface.

There is no one true input for the Web. We have to contend with fingers, mice, keyboards, voice and more. The challenge for us over the next few years is not designing for one input but many.

### Touch

Touch is no longer just isolated to smartphones and tablets. Many big sreens in laptops or desktops nowadays are touch capable. Every desktop design has to be touch-friendly now.

The optimal touch target size is 7mm, based on the average size of human finger tips and pads. CSS2.1 defines a pixel as 1/96 of an inch. So 7mm should be 30pixels [Designing for Touch]. However, things aren’t so easy because of dynamic viewports. It means that input elemtents in website have to be usually bigger.

The best touch interface is sometimes no touch at all. We can use sensors and speech input which is the next frontier for interaction design.

### Speech

The speech input aims to provide an alternative input method for web applications, without using a keyboard or other physical device. This is no longer science fiction but reality. Many companies rely on it and deploy it to the modern devices and software. It could be also benefitial for older or disabled users [Speech Recognition and Alternative Interfaces] and can easily become the next big thing.

We can now use speech recognition to take a full control of the web site as we have access to continuous recognition stream. We don't need another input methods at all. A speech feedback for user interaction is also important and we can use speech synthesis feature for it.

### Device motion

We can use a lot of sensors in the devices to detect the device motion. It is made possible by a combination of always-on sensors as are an accelerometer a gyroscope, and a magnetometer, that tell us a lot about how a device is moving through the space around it. The ability of these sensors to provide precise information about the movement of a device opens up new design possibilities for web applications [Re-imagining Apps for Ultrabook].

From controlling the user interface based on three dimensional motion as input, to combining device motion with another sensors as are location detection or video cameras, there's a lot of interesting interface designs made possible by Device Motion. It depends on us how we use them.

### Video Motion

Many modern devices contains built in video camera sensor which we can use as alternative method to device motion. We can access video stream and analyse landscape around the device. Video motion detection is a way of defining user activity in a scene by analyzing image data and differences in a series of images.

We can detect user motion and use it as an alternatove part of input method. We can build web games and another real time interfaces. There's again a lot of interesting interface designs made possible.

## Adaptive Web Components

One of the most common critiques against responsive Web design is that it creates large (file size) Web sites, thereby slowing Web pages down. But we can make responsive sites perform well, we just have to the work to make it possible. [20MB Responsive Websites]

We care about mobile performance because people need fast experiences on the Web. There's lot of studies that highlight the importance of speed. More than half of people with a bad loading experience on mobile, won't come back.
Speed is a feature. You can quantify its impact on the metrics you care about. [High Performance Browser Networking]

We all should care about page speed. 73% of mobile internet users say they've encountered Web pages that are too slow. A 1 second delay can result in a 7% reduction in conversions.
Mobile network speeds have gone up but this doesn't help much as page load times tend to plateau as bandwidth increases. Latency is a much bigger contribution to download times. LTE reduces tower latency by several milliseconds but we still need to make a number of connections to get data to your phone. [Page Speed is Only the Beginning]

Web components allow you to use custom HTML elements in the browser. You can wrap up a simple element or an entire application within an HTML element. Web components allows you to build Web applications in a modular, reusable, and encapuslated way.

## Evaluation and experiments 

There has been made a serie of experiments on both adaptive input methods and components. All of them have been released as open source reusable modules on GitHub.

### Input methods

### Components

So what are we to do? This is actually a great opportunity to utilize conditional loading to serve the best experience for the right context.

A static default. We can then use Javascript to detect when it’s appropriate to introduce the embedded map. After all, embedded maps work quite well when there’s enough room to maneuver within them. We can simply replace the default experience with the iframe map when enough screen real estate becomes available.

By default we can simply include a text link to the location on the Google Maps website. And in case a “View Map” text link isn’t attractive enough for you, we can also use the Static Maps API to pull in a static image of the location.

When a user taps the link, most major mobile platforms will fire up the native maps application where the user can have a richer experience. If the native experience is unavailable, the user is simply taken to the Google Maps website, where they receive a dedicated full-screen mapping experience. Either way, it’s a better experience than a cramped embedded map.

This approach works quite well for simple map plotting and even showing groups of locations. However, more interactive mapping requires additional consideration, but even then I’d say that an embedded map still might not make sense. While techniques like adaptive maps might not make sense in every circumstance, it’s a decent baseline.

## Conclusion

More changes are coming, new APIs and beyond. What will you do with this new power? An innovator is someone who wakes up to the constraints caused by false assumptions, and breaks out of them.

## Refereneces

1.  Luke Wroblewski - Mobile First. ISBN: 978-1-937557-02-7
2.  Luke Wroblewski - Re-imagining Apps for Ultrabook. Intel Software 2013
-   Ethan Marcotte - Responsive Web Design. ISBN: 978-0-9844425-7-7
-   Jason Grigsby - Adaptive Input. Breaking Development in San Diego CA 2013
-   Brad Frost - Beyond Squishy: The Principles of Adaptive Design. SXSW conference, Austin, TX, USA 2013
-   Aaron Gustafson - Building Adaptive Designs Now. User Interface 17, Boston, MA 2012
-   Mat Marquis - 20MB Responsive Websites. Breaking Development in Orlando FL 2013
-   Josh Clark - Designing for Touch. An Event Apart in Seattle, WA 2013
-   Ilya Grigorik - High Performance Browser Networking, ISBN: 9781449344764 O'Reilly Media, Incorporated. 2013
-   Peter McLachlan - Page Speed is Only the Beginning. Breaking Development in San Diego CA 2013
-   Basson, Sara and Fairweather, Peter G. and Hanson, Vicki L. - Speech Recognition and Alternative Interfaces for Older Users. ACM 2007
-   Kratz, Sven and Rohs, Michael and Essl, Georg - Combining Acceleration and Gyroscope Data for Motion Gesture Recognition Using Classifiers with Dimensionality Constraints. Proceedings of the 2013 International Conference on Intelligent User Interfaces. 2013
  

