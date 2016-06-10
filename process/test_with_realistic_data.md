# Test With Realistic Data

We're thankful for all of the tools that allow us to get a development environment set up quickly. It is important however, not to be lulled into a false sense of security by the ease with which our code runs in development.

## New Applications

Completely new applications run the greatest risk of encountering data issues, simply because the code has not yet been run against data generated "in the wild." Your code may run fine with a very small amount of data in the database, but until it is run against a considerably larger amount generated after launch, you won't know how well your code holds up.

The way to avoid a slow or unresponsive application after launch — and the need to support such scenarios under high pressure — is to test beforehand with realistic data.

Work with users to determine likely characteristics of the data, such as which tables might have the highest number of rows, or which columns might contain large amounts of text or binary data.

Create a task that uses factories or otherwise generates records for the objects in the application. Commit this task to version control so that other developers can also quickly and easily populate their local database with a set of realistic data. Keep this task up to date with changes to the data model and anticipated usage characteristics.

If possible, have users create data as part of their testing in a staging environment. While the content of this data will be more realistic than data you might generate purely from factories or other automated methods, in most cases it will still not be of sufficient size to test the application thoroughly. You can maintain the nature of the content while scaling out the size of the data by writing a task to duplicate this existing user data many times over.

## Existing Applications

When working on an existing application, it is important to make sure that changes don't negatively impact performance. The advantage that existing applications have is that you usually already have a production database populated with real-world data.

Ensure that you and your team have easy access to backups of this data, and a simple process for importing it into your development environment, for the purposes of testing changes.

## Resolving Issues

Issues identified by testing with realistic data can often be fixed by a handful of approaches.

- [Identifying][bullet] and [eliminating][eager-loading] N+1 queries
- [Identifying][explain] and [adding][migrations] beneficial indexes
- [Query optimization][query-optimization]
- [Caching][caching]

[bullet]: https://github.com/flyerhzm/bullet
[eager-loading]: http://guides.rubyonrails.org/active_record_querying.html#eager-loading-associations
[explain]: https://www.foraker.com/blog/examining-slow-queries-with-explain-analyze
[migrations]: http://api.rubyonrails.org/classes/ActiveRecord/Migration.html
[query-optimization]: https://www.amazon.com/PostgreSQL-High-Performance-Gregory-Smith/dp/184951030X
[caching]: http://guides.rubyonrails.org/caching_with_rails.html
