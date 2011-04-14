# JSON PHP

This is a pure PHP JSON library. If you can, you should `pear install json`,
and forget this library exists. However, if you're developing in an
environment where you aren't able to install JSON via pear, this library
can be used to provide JSON support.


## Usage

    /**
     * Provides a pure PHP json_decode function
     */

    if ( ! function_exists('json_decode')) {
      require_once('JSON.php');
      function json_decode($var) {
        $JSON = new Services_JSON;
        return $JSON->decode($var);
      }
    }

    // ----------------------------------------------------------------------

    /**
     * Provides a pure PHP json_encode function
     */

    if ( ! function_exists('json_encode')) {
      require_once('JSON.php');

      function json_encode($var) {
        $JSON = new Services_JSON;
        return $JSON->encode($var);
      }
    }


## Credit

Michal Migurski - <http://pear.php.net/pepr/pepr-proposal-show.php?id=198>
