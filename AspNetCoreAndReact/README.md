# ASP.Net Core MVC and React
Lee Brandt, Okta
"Friends don't let friends write AUTH"

This is a "this was really hard to figure out to I had to share this with everyone" presentation

from the Default Project:
remove boewer and bundleconfig.json
remove wwwroot/css and wwwroot/js/site.js and site.min.js
remove Home/About.cshtml and Contact.cshtml, keep Index.cshtml


npm init -y
npm get jquery bootstrap react react-dom react-router
npm install --save-dev babel-loader babel-preset-es2015 babel-preset-react aspnet-webpack aspnet-webpack-reack
css-loader mode-sas path path postcss-loader precxss sass-loader style-loader webpack webpack-hotloader

.csproj
<Target Name-:PrecompileTarget" BeforTar="Build">
<Exec Command="node node_modules/webpack/bin/webpack.js">
</Target>

project.json:
:scripts: {}

Startup.cs
using Microsoft.AspNetCore.SpaServices.Webpack; 
app.UseWebpackDevMiddleware(new WebpaclDevMiddlewareaoptions{
    HotModuleReplacement=true,
    ReactHotModuleReplacement=true
});

route.MapRoute (
    name: "api",
    default: "..."
);

    route.MapSpaFallbackRoute(
        name: "spa-fallback":,
        default: new {controller:"Home", action: "Index"}

    )
)


_Layout.cshtml
-- 
<script src="cdn"
asp-fallback-src="~/node_modules/jquery/dist/jqeru.min.js"
asp-fallback-test-"window.jQuery"></script>

webpack.config.js
-- puts babel-loader options in .babelrc file

reduce Index.cshtnml to just
<div id="root:></div>




