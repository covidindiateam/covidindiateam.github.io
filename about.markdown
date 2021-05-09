---
layout: page
title: About
permalink: /about/
---

```c
/* API message handlers */
static void vl_api_upf6_adj_add_t_handler(vl_api_upf6_adj_add_t * mp)
{
  vl_api_upf6_adj_add_reply_t * rmp;
  upf6_main_t * ump = &upf6_main;
  int rv = 0;

  ip_address_t ip = ip_address_initializer;
  ip_address_decode2 (&mp->ip, &ip);
  rv = upf6_adj_add (ntohl(mp->sw_if_index), &ip);
  REPLY_MACRO(VL_API_UPF6_ADJ_ADD_REPLY);
}
```
Our mission is to save lives.

We are a team of volunteers from different walks of life with varied experiences, diverse skills but with a common mission of saving lives during the current COVID-19 surge in India.

Our charter evolves as we identify areas that are critical to our mission. At present, it includes but is not limited to the following:



