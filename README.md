# A Webpack loader for resolving KMT urls

Using `webpack-dev-server` with KMT you need to fix some urls else they will not work... We actually need to emulate the framework within the `webpack-dev-server`.

hence this... 

> IMPORTANT: This is only needed for development!

> WARNING: This loader will not (yet) work for encore dev-server as 
> it works in the reverse... this would require something
> that redirects back to the referrer...? In any case worthy of an issue, to be resolved ;-)

## Usage

Add the loader

    yarn add @kingsquare/webpack-kmt-resolve-url-loader

Until then just add the repo ;-)

Then after the `resolve-url-loader` add the `kmt-resolve-url-loader`

      {
        loader: "kmt-resolve-url-loader",
        options: {
          sourceMap: true,
          root: path.resolve(__dirname, "../view/layout")
        }
      }
