# 网页文章

## 未读
```dataview
table
from "Read It Later"
where !contains(tags, "#Readed") and !contains(tags, "#Reading") and Readed != true
sort file.name asc
```

## 正在读
```dataview
table tags
from "Read It Later"
where contains(tags, "#Reading")
sort file.name asc
```

# 视频

## 未看
```dataview
table
from "Watch It Later"
where Archived != true
sort file.name asc
```

## 正在看
```dataview
table tags
from "Watch It Later"
where contains(tags, "#Watching")
sort file.name asc
```

