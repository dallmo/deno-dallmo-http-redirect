# overview
a deno module for simple http redirections

# usage

## 1. simple / fixed / single target redirect
```
import {dallmo_http_redirect} from "https://deno.land/x/dallmo_http_redirect/mod.ts"

const to_hostname: string = "dallmo.com";
dallmo_http_redirect( to_hostname );
```

## 2. conditional redirection mappings
```
import {dallmo_http_redirect} from "https://deno.land/x/dallmo_http_redirect/mod.ts"

const redirect_mapping_conf = "redirect_mappings.yaml";
dallmo_http_redirect( redirect_mapping_conf );
```

sample yaml file content :
```
---
- in: okok.com 
  to: 123.com

- in: aaa.com
  to: bbb.net
```

i.e. 
- the key `in` stands for `incoming request`, where the requested host is specified.
- the key `to` is where this request will be redirected to.
