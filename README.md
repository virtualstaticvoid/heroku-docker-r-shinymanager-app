# Issue #142

https://github.com/virtualstaticvoid/heroku-buildpack-r/issues/142

## Description

[From issue description](https://github.com/virtualstaticvoid/heroku-buildpack-r/issues/142#issue-689547054):

> I'm currently using this build-pack to host a shiny application on Heroku.
> I need this app to have some basic authentication, so I found a library called "shinymanager" which works exactly like I want it too.
> This library is hosted on the CRAN and can be found [here](https://cran.r-project.org/web/packages/shinymanager/index.html).
>
> I first tried to install shiny manager through the recommended init.R file using the helpers.installPackages() command.
> This did not work, so I then tried to install shiny manager locally by including the tar.gz file in my build.
> I tried putting it in the main directory, as well as creating a folder called _localpckgs_, neither of these worked.
> I also made sure to include "/app" in front of the path of the file, this also did not work.
>
> I'm not sure why this package won't install, every time I build I get the error "there is no library called shinymanager".
> I think it works with the R version being used, so not sure what other issues there could be.
