# Ajaxify
This is a modified version of the original [Ajaxify plugin](https://github.com/browserstate/ajaxify) that is customized to work for the default code structure of the [_s (Underscores)](http://underscores.me/) WordPress theme. It is assumed that you are using the _s theme and have not modified the basic structure, classes or IDs provided in the theme. 

## Installation

In order for this to work, you’ll need to use wp_enqueue_script() to include the [History.js](https://github.com/browserstate/history.js) and [scrollTo](https://github.com/balupton/jquery-scrollto) libraries, as well as my modified Ajaxify script. Do this in your existing enqueue function. If you don’t know what that means, check out this article.

    wp_enqueue_script( 'scrollto', '//balupton.github.io/jquery-scrollto/lib/jquery-scrollto.js', array( 'jquery' ), '', true );
    wp_enqueue_script( 'history-js', '//browserstate.github.io/history.js/scripts/bundled/html4+html5/jquery.history.js', array(), '', true ); 
    wp_enqueue_script( 'ajaxify', '//raw.githubusercontent.com/AbacusPowers/ajaxify_s/master/ajaxify-html5.js', array( 'jquery' ), '', true ); 
    
Above, you’ll find the lines to include, if you want to load these libraries remotely. I would recommend, however, that you actually take the time to download them, and use a filepath specific to your theme. You can use something like

    wp_enqueue_script( 'ajaxify', get_template_directory_uri() . '/js/vendor/ajaxify_s/ajaxify-html5.js', array( 'jquery' ), '', true );
instead of the direct link to the library on GitHub.


## License

Licensed under the [New BSD License](http://opensource.org/licenses/BSD-3-Clause)
