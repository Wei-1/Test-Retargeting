# Note - 2021-06-08

This test and API link is no longer working.

Stop the repo maintenance.

----

# W?

This is a repo for Google Doubleclick (DC) Retargeting API testing.

## Usage

One will get a `google_nid` after you ask DC for it. The `google_nid` can be used in the url below:

```bash
# let's say your nid is "A_NICE_NID"
curl https://cm.g.doubleclick.net/pixel?google_nid=A_NICE_NID&google_cm&para1=123&para2=abc
```

The request will be redirected to

```
https://your.end/point?para1=123&para2=abc&google_gid=CAESELbN5asdfqwer9876543210&google_cver=1
```

People are using this api provided by DC to sync users.

## Machenism

1. We -> apply for NID -> DC (provide end-point to Google for redirection)

2. DC -> provide NID -> We

3. End-user -> trigger Link with NID -> DC -> redirect to your end-point with google_gid -> We

##### P.S.

Example is tested with Groundhog Technologies Inc's end-point
