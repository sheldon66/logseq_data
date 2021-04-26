---
title: nginx
---

## nginx mobile auto redirect
```sh
location /
{
      if ($http_user_agent ~* '(iPhone|iPod|android|blackberry)')
      {
        rewrite ^ http://m.tansun.com.cn/mobile$request_uri? redirect;
        break;
      }
}
```
