# altv-notifications

---

![](https://github.com/godkoten/altv-notifications/raw/master/1.png)

---

# Example

### Client

resource.cfg
```
deps: [
	notifications
]
```

index.mjs
```javascript
import * as notifications from 'notifications';
notifications.show('Hello', false, 134);
notifications.showWithPicture('Youtube', '', 'www.youtube.com', 'CHAR_YOUTUBE', 1, false, -1, 6);
```



### Server
```javascript
alt.emitClient(null, 'notifications:show', 'Hello', false, 134);
alt.emitClient(null, 'notifications:showWithPicture', 'Youtube', '', 'www.youtube.com', 'CHAR_YOUTUBE', 1, false, -1, 6);
```

---
# Document
## show

message: Message  
flashing: Flash  
textColor = [Text color](https://wiki.rage.mp/index.php?title=Fonts_and_Colors)  
bgColor = [Background color](https://wiki.rage.mp/index.php?title=Fonts_and_Colors)  
flashColor: [red, green, blue, alpha], Need flashing true  

---
## showWithPicture

title: Title    
sender: Sender  
message: Message  
notifPic: [NotifPic](https://wiki.gtanet.work/index.php?title=Notification_Pictures)  
iconType = [IconType](#Icons)  
flashing = Flash  
textColor = [Text color](https://wiki.rage.mp/index.php?title=Fonts_and_Colors)  
bgColor = [Background color](https://wiki.rage.mp/index.php?title=Fonts_and_Colors)  
flashColor = [red, green, blue, alpha], Need flashing true  


---
<h1 id="Icons">Icons</h2>

```
0, 4, 5, 6 = No Icon  
1 = Speech Bubble  
2 = Message  
3 = Friend Request  
7 = Arrow  
8 = RP  
9 = Money  
```
---
