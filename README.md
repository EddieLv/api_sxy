``` r
if (!require(remotes))
    install.packages("remotes")
remotes::install_github("EddieLv/openai")
```

## Authentication

To use the OpenAI API, you need to provide an API key. First, sign up
for OpenAI API on [this page](https://openai.com/api/). Once you signed
up and logged in, you need to open [this
page](https://platform.openai.com), click on **Personal**, and select
**View API keys** in drop-down menu. You can then copy the key by
clicking on the green text **Copy**.

By default, functions of `{openai}` will look for `OPENAI_API_KEY`
environment variable. If you want to set a global environment variable,
you can use the following command (where
`xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` should be replaced
with your actual key):

``` r
#跟数信院客服领取独享key
Sys.setenv(
    OPENAI_API_KEY = 'xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx'
)
```
