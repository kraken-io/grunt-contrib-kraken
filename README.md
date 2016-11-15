grunt-kraken
====================

Grunt plugin to optimize all your images with the powerful Kraken.io API

````
var grunt = require('grunt');

grunt.initConfig({
    kraken: {
        options: {
            key: 'kraken-api-key-here',
            secret: 'kraken-api-secret-here',
            lossy: true
        },

        dynamic: {
            files: [{
                expand: true,
                cwd: 'src/images/',
                src: ['**/*.{png,jpg,jpeg,gif}'],
                dest: 'dst/images-optimized/'
            }]
        }
    }
});

grunt.loadNpmTasks('grunt-contrib-kraken');
grunt.registerTask('default', ['kraken']);
````
