This project extends the functionality of a simulated music streaming platform by implementing features like Wrapped statistics, monetization
notifications, and recommendations, using various design patterns to ensure modularity and flexibility.
Wrapped:

    The "Wrapped" feature, which generates yearly summaries for users, artists, and hosts, follows a Command Pattern.
    All three Wrapped command types implement a common interface, WrappedCommand, allowing for polymorphic behavior and easy invocation of commands.
    User statistics are dynamically updated in the StatisticsWrapped object each time the song in the player changes.

Monetization:

    MonetizationStatistics: This static object stores all data related to artist earnings.
    Each user has a MonetizationCalculator in their Player, which tracks the costs associated with the songs they listen to.
    Payments can be made either through listening to ads or by subscribing to a premium service.

Notifications:

    Notifications follow an Observer Pattern. Artists maintain a list of followers, enabling them to notify users when necessary.
    This functionality is encapsulated within the page_elements package as notifications are primarily used on the homepage.

Recommendations:

    Similar to the SearchBar object, the Recommendation object generates content suggestions based on user preferences.
    Results are stored in this object and can be accessed as required.

Other Design Patterns:

    The Singleton Pattern is used for the Admin object, ensuring a single instance throughout the application.
    A Factory Pattern is used to create new users via the "addUser" command, simplifying user creation and management.

Summary:

This project leverages multiple design patterns, including Command, Observer, Singleton, and Factory,
 to implement key features like Wrapped statistics, artist monetization, notifications, and content recommendations.
  These additions provide robust functionality and enhance the user experience on the platform.