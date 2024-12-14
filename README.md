``` r
if (!require(remotes))
    install.packages("remotes")
remotes::install_github("irudnyts/openai", ref = "r6")
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
Sys.setenv(
    OPENAI_API_KEY = 'xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx'
)
```
``` r
voice_sample_ua <- system.file("extdata", "sample-ua.m4a", package = "openai")
create_translation(file = voice_sample_ua, model = "whisper-1")
#> $text
#> [1] "I want to check how this model works"
```
