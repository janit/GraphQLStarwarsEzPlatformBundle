
# Import eZ Platform data schema for GraphQL Star Wars example

This is an example of data used by the Kaliop eZ Migrations Bundle for eZ Platform (and eZ Publish 5.x).

## Installation

First install the [eZ Migrations Bundle](https://github.com/kaliop-uk/ezmigrationbundle/) and then clone
this bundle to your src directory and enable the bundle in your application kernel:

    public function registerBundles()
    {
        $bundles = array(
            ... more stuff here ...
            new GraphQLStarwarsEzPlatformBundle\GraphQLStarwarsEzPlatformBundle(),
        );
    }
    
Once you have this installed, then you can use the kaliop migrations to execute the migration:

     php ezpublish/console kaliop:migration:update

Once this is complete, then you should have content objects in your database that corresponds to
to the examples that are used by the [GraphQL examples](https://github.com/graphql/graphql-js).

This bundle does not expose a GraphQL interface to the created data, but just contains the data
structure itself. This can be implemented in the future using the groundwork available for 
[Symfony and GraphQL](https://www.symfony.fi/entry/graphql-with-php-and-the-symfony-framework).