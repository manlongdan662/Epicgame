# EpicGames 自动白嫖每周免费游戏
![image](https://user-images.githubusercontent.com/4411977/74479432-6a6d1b00-4eaf-11ea-930f-1b89e7135887.png)

# 禁止将本程序用于盈利,如有需求请自行对使用MIT协议开源的原Repo进行修改。
# 使用本程序即意味着,您使用过程中如果违法相关法律法规和用户协议,作者不承担相应责任。
## 使用过程
0. 先给这个仓库来个Star（笑
1. 下载[DeviceAuthGenerator](https://github.com/xMistt/DeviceAuthGenerator/releases/)
2. 运行程序,在出现的页面里登录Epic账户,然后授权。完成后会出现一个 `device_auths.json`文件
3. Fork或者手动导入这个Repo,看你喜好(防止被Github一锅端)
4. 启用Actions,新建一个叫做`AUTH_JSON`的Secret,并将之前的`device_auths.json`文件内容粘贴进去。
5. 修改.github/workflows/claim.yml文件,改改自动领取时间什么的。

## 多账户
最后获得的json大概长这样

```
{
    "mcseekeri": {
        "device_id": "114514",
        "account_id": "1919810",
        "secret": "893",
        "user_agent": "DeviceAuthGenerator/1.1.0 Windows/10.0.19041",
        "created": {
            "location": "Neverland",
            "ip_address": "114.51.45.14",
            "datetime": "1970-01-01T00:00:00.000Z"
        }
    }
}
```

如果要多账户签到,那么需要修改成这样。

```
{
    "mcseekeri": {
        "device_id": "114514",
        "account_id": "1919810",
        "secret": "893",
        "user_agent": "DeviceAuthGenerator/1.1.0 Windows/10.0.19041",
        "created": {
            "location": "Neverland",
            "ip_address": "114.51.45.14",
            "datetime": "1970-01-01T00:00:00.000Z"
        }
    },
    "mcseekeri2333": {
        "device_id": "114514",
        "account_id": "1919810",
        "secret": "893",
        "user_agent": "DeviceAuthGenerator/1.1.0 Windows/10.0.19041",
        "created": {
            "location": "Neverland",
            "ip_address": "114.51.45.14",
            "datetime": "1970-01-01T00:00:00.000Z"
        }
    }
}
```

可以使用[Sojson工具](https://www.sojson.com/)进行格式检查,保证语法合法性。
# 致谢
感谢Revadike大佬的[epicgames-freebies-claimer](https://github.com/Revadike/epicgames-freebies-claimer),本Repo是在他程序的基础上修改而来的。