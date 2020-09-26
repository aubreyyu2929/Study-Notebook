# pathlib包比os更优雅更快捷
python3.4+ 都自带标准库pathlib，所以你不需要再通过pip3 安装
官方包文档：https://docs.python.org/3/library/pathlib.html

实例
```
from pathlib import Path

data_folder = Path("source_data/text_files/")

file_to_open = data_folder / "raw_data.txt"

f = open(file_to_open)

print(f.read())

```

当我们需要读文件时，不需要打开就可以直接读
```
from pathlib import Path

data_folder = Path("source_data/text_files/")

file_to_open = data_folder / "raw_data.txt"

print(file_to_open.read_text())
```

```
from pathlib import Path

filename = Path("source_data/text_files/raw_data.txt")

print(filename.name)
# prints "raw_data.txt"

print(filename.suffix)
# prints "txt"

print(filename.stem)
# prints "raw_data"

if not filename.exists():
    print("Oops, file doesn't exist!")
else:
    print("Yay, the file exists!")
```

搬运自：https://zhuanlan.zhihu.com/p/33524938
