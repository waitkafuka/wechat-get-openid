# 微信网页获取用户 openid 的最简代码

# 对应后端代码：

```javascript
const getOpenId = async function (code) {
  // https://api.weixin.qq.com/sns/oauth2/access_token?appid=APPID&secret=SECRET&code=CODE&grant_type=authorization_code
  const { data } = await axios.get('https://api.weixin.qq.com/sns/oauth2/access_token', {
    params: {
      appid: config.wechatPay.appid,
      secret: config.wechatPay.secret,
      code,
      grant_type: 'authorization_code',
    },
  });
  return data;
};
```
