# Sass-debug-partial
A partial to debug layout issues in the browser.

Adds a black border around all the elements and a red border to any elements that can receive keyboard focus (tab index).

## Usage

In your main scss-file, just import the _debug.scss partial.

    @import 'debug';

If you're using Jekyll, I recommend adding a debug flag in your _config.yml
    debugscss: true
    
and wrapping your import statement into an if statement

    {% if site.debugscss == true %}
        @import 'debug';
    {% endif %}
    
Or alternatively have a separate _debug_config.yml with

    debugscss:true
    
and run jekyll with the --config flag 

    jekyll build --config "_config.yml,_debug_config.yml"
