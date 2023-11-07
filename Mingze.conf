# 自用Quantumult X配置

[general]
# 对指定的网址进行相应测试，以确认节点的可用性
server_check_url=http://cp.cloudflare.com/generate_204
# 资源解析器
resource_parser_url=https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
# 节点页面的信息展示
geo_location_checker=http://ip-api.com/json/?lang=zh-CN, https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/IP_API.js
# dns_exclusion_list
dns_exclusion_list = *.qq.com, qq.com
# 下列表中内容将不经过 QuantumultX 的处理
excluded_routes=192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, 17.0.0.0/8
icmp_auto_reply=true
[dns]
# DoH服务器(DNS over HTTPS)
doh-server=https://doh.360.cn/dns-query
# 常规DNS服务器
# Google DNS
server=8.8.8.8
server=8.8.4.4
# 114 DNS
server=114.114.114.114

[policy]
## 策略组
# FINAL策略：如果以下策略均未被匹配到，则听从此策略
static=Final, proxy, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Final01.png
# 自动选择香港最优节点
## 地区分组策略
# 美国
url-latency-benchmark=US, server-tag-regex=美国|波特兰|达拉斯|俄勒冈|凤凰城|费利蒙|硅谷|拉斯维加斯|洛杉矶|圣何塞|圣克拉拉|西雅图|California|芝加哥|🇺🇸|United States|US, check-interval=600, tolerance=0, alive-checking=false, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Country/US.png
# 日本
url-latency-benchmark=JP, server-tag-regex=日本|东京|Tokyo|大阪|埼玉|🇯🇵|JP|Japan, check-interval=600, tolerance=0, alive-checking=false, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Country/JP.png
# 香港
url-latency-benchmark=HK, server-tag-regex=HK|香港|🇭🇰️|中港|沪港|Hong, check-interval=600, tolerance=0, alive-checking=false, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Country/HK02.png
# 台湾
url-latency-benchmark=TW, server-tag-regex=台|台湾|Taiwan|TW, check-interval=600, tolerance=0, alive-checking=false, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Country/TW02.png
# 新加坡
url-latency-benchmark=SG, server-tag-regex=狮城|新加坡|Singapore|🇸🇬|SG, check-interval=600, tolerance=0, alive-checking=false, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Country/SG.png
# 国外媒体细分策略
# > Netflix策略
url-latency-benchmark=Netflix, server-tag-regex=台湾|新加坡, check-interval=600, tolerance=0, alive-checking=false,img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Netflix.png
# > Disney策略
url-latency-benchmark=Disney, server-tag-regex=日本|台湾, check-interval=600, tolerance=0, alive-checking=false, img-url=https://user-images.githubusercontent.com/125243935/280790130-6a435631-bdb5-4cca-91c6-24db35b58059.png
# > YouTube策略
static=YouTube, HK,img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Youtube.png
# > Spotify策略
static=Spotify, US, HK, TW, SG, Final, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Spotify.png
# 软件&服务策略
# > Telegram策略
static=Telegram, SG, JP, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Telegram.png
# > Twitter策略
static=Twitter, US, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Twitter.png
# > Instagram策略
static=Instagram, US, HK, JP, SG, Final, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Instagram.png
# > Speedtest策略
static=Speedtest, US, HK, JP, TW, SG, Final, proxy, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Speedtest.png
# > Apple策略
static=Apple, US, HK, JP, TW, SG, Final, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Apple.png
# > Google策略
static=Google, US, TW,img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Google.png
# > Microsoft策略
static=Microsoft, US, HK, JP, TW, SG, Final, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Microsoft.png
# Mainland策略-国内访问
static=Mainland, HK, proxy, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Mainland.png
# Global策略
static=Global, US, Final, direct, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/Outside.png
[filter_remote]
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/OpenAI/OpenAI.list, tag=OpenAI, force-policy=SG, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/WeChat/WeChat.list, tag=WeChat, force-policy=direct, update-interval=172800, opt-parser=true, enabled=true
## 远程分流规则订阅
# Netflix规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Netflix/Netflix.list, tag=Netflix 规则, force-policy=Netflix, update-interval=172800, opt-parser=true, enabled=true
# Spotify规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Spotify/Spotify.list, tag=Spotify 规则, force-policy=Spotify, update-interval=172800, opt-parser=true, enabled=true
# YouTube规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/YouTube/YouTube.list, tag=YouTube 规则, force-policy=YouTube, update-interval=172800, opt-parser=true, enabled=true
# Speedtest规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Speedtest/Speedtest.list, tag=Speedtest 规则, force-policy=Speedtest, update-interval=172800, opt-parser=true, enabled=true
# Telegram规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Telegram/Telegram.list, tag=Telegram 规则, force-policy=Telegram, update-interval=172800, opt-parser=true, enabled=true
# Twitter规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Twitter/Twitter.list, tag=Twitter, force-policy=Twitter, update-interval=172800, opt-parser=true, inserted-resource=true, enabled=true
# Instagram规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Instagram/Instagram.list, tag=Instagram 规则, force-policy=Instagram, update-interval=172800, opt-parser=true, enabled=true
# BiliBili规则
# Apple规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Apple/Apple.list, tag=Apple 规则, force-policy=Apple, update-interval=172800, opt-parser=true, enabled=true
# Google规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Google/Google.list, tag=Google 规则, force-policy=Google, update-interval=172800, opt-parser=true, enabled=true
# Microsoft规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Microsoft/Microsoft.list, tag=Microsoft 规则, force-policy=Microsoft, update-interval=172800, opt-parser=true, enabled=true
# Mainland规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/China/China.list, tag=Mainland 规则, force-policy=Mainland, update-interval=172800, opt-parser=true, enabled=true
# Global规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/release/rule/QuantumultX/Global/Global.list, tag=Global 规则, force-policy=Global, update-interval=172800, opt-parser=true, enabled=true
#Disney规则
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/release/rule/QuantumultX/Disney/Disney.list, tag=Disney 规则, force-policy=Disney, update-interval=172800, opt-parser=true, enabled=true

[filter_local]
# 本地分流规则 相同规则下本地规则优先生效
# 国内分流
geoip, cn, Mainland
# 内部网络直连
host-suffix, local, direct
# Giffgaff
host-suffix, giffgaff, direct
#final
final, Final 

[server_local]
# 本地服务器节点
[server_remote]
https://fenda.ink/link/IUxgb1OjYH1wHast?list=quantumultx, tag=Fendacloud, update-interval=172800, opt-parser=false, enabled=true
https://rsslinghun1.xyz/api/v1/client/subscribe?token=54674e2e784e7785eaeb64a4f86e7c4a, tag=灵魂云, update-interval=172800, opt-parser=false, enabled=true

[rewrite_remote]
https://raw.githubusercontent.com/DivineEngine/Profiles/master/Quantumult/Rewrite/Block/YouTubeAds.conf, tag=YouTube去广告, update-interval=172800, opt-parser=true, enabled=true
# 远程重写订阅
# Spotify解锁
https://raw.githubusercontent.com/app2smile/rules/master/module/spotify.conf, tag=Spotify, update-interval=172800, opt-parser=true, enabled=true
# BoxJs模块
https://github.com/chavyleung/scripts/raw/master/box/rewrite/boxjs.rewrite.quanx.conf, tag=BoxJS, update-interval=-1, opt-parser=false, enabled=false
# Sub-Store模块
https://raw.githubusercontent.com/Peng-YM/Sub-Store/master/config/QX.snippet, tag=Sub Store, update-interval=172800, opt-parser=true, enabled=true

[rewrite_local]
# 本地重写

[task_local]
# 脚本任务
event-interaction https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/streaming-ui-check.js, tag=流媒体解锁, img-url=https://raw.githubusercontent.com/fanmingming/Rules/main/Filter/GMedia.png, enabled=true

[mitm]
# 开启 mitm，需要自行在Quantumult X中生成证书、安装、信任
passphrase = 
p12 = 
hostname = sub.store
