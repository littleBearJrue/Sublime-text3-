# Ctags插件的使用
## 安装步骤
1. 首先sublime需要安装package control
2. 按住快捷键ctrl+shift+p调出package control,输入关键字"ip"，找到install package,点击等待弹出框
3. 在弹出框中输入"Ctags",找到并点击安装即可

## 优化插件
为了更方便的服务于我们的开发工作，我们需要对默认的CTags插件进行优化处理
1. 点击"Preferences"，依次找到Package Settings -> CTags -> Settings-User,打开Settings-User文件
2. copy以下代码到文件中保存即可
```
// Place your settings in the file "User/CTags.sublime-settings", which
// overrides the settings in here.
{
    // Enable debugging
    "debug": false,

    // Enable autocomplete
    "autocomplete": false,

    // Alter this value if your ctags command is not in the PATH, or if using
    // a different version of ctags to that in the path (i.e. for OSX).
    //
    // NOTE: You *should not* place entire commands here. These commands are
    // built automatically using the values below. For example:
    //   GOOD: "command": "/usr/bin/ctags"
    //   BAD:  "command": "ctags -R -f .tags --exclude=some/path"
    "command": "C:\\Windows\\System32\\ctags58\\ctags.exe",

    // Set to false to disable recursive search for ctag generation. This
    // translates the `-R` parameter
    "recursive" : true,

    // Default read/write location of the tags file. This translates to the
    // `-f [FILENAME]` parameter
    "tag_file" : ".tags",

    // Additional options to pass to ctags, i.e.
    // ["--exclude=some/path", "--exclude=some/other/path", ...]
    // "opts" : ["--regex-LUA='/^.*\\s*function\\s*(\\w+):(\\w+).*$/\\2/f/'","--regex-LUA='/^\\s*(\\w+)\\s*=\\s*[0-9]+.*$/\\1/e/'","--regex-LUA='/^.*\\s*function\\s*(\\w+)\\.(\\w+).*$/\\2/f/'", "--regex-LUA='/^.*\\s*function\\s*(\\w+)\\s*\\(.*$/\\1/f/'","--languages=LUA","--regex-LUA=/^\\s*(\\w+)\\s*=\\s*\\{.*$/\\1/e/","--regex-LUA=/^\\s*module\\s+\"(\\w+)\".*$/\\1/m,module/","--regex-LUA=/^\\s*module\\s+\"[a-zA-Z0-9._]+\\.(\\w+)\".*$/\\1/m,module/"],
    // "opts" : "--langdef=LUA --langmap=LUA:.lua --regex-LUA=/^.*\\s*function\\s*(\\w+):(\\w+).*$/\\2/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*[0-9]+.*$/\\1/e/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\.(\\w+).*$/\\2/f/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\s*\\(.*$/\\1/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*\\{.*$/\\1/e/ --regex-LUA=/^\\s*module\\s+\"(\\w+)\".*$/\\1/m,module/ --regex-LUA=/^\\s*module\\s+\"[a-zA-Z0-9._]+\\.(\\w+)\".*$/\\1/m,module/ --languages=LUA",
    "opts":[
    // "--langdef=LUA",
    // "--langmap=LUA:.lua",

    "--regex-LUA=/^.*\\s*function\\s*(\\w+):(\\w+).*$/\\2/f/",
    "--regex-LUA=/^.*\\s*function\\s*(\\w+)\\.(\\w+).*$/\\2/f/", 
    "--regex-LUA=/^(\\w+)[.](\\w+)\\s*=\\s*function.*$/\\2/f/",
    "--regex-LUA=/^.*\\s*function\\s*(\\w+)\\s*\\(.*$/\\1/f/",
    "--regex-LUA=/^\\s*(\\w+)\\s*=\\s*[0-9]+.*$/\\1/e/",
    "--regex-LUA=/^\\s*(\\w+)\\s*=\\s*\\{.*$/\\1/e/",
    "--regex-LUA=/^\\s*module\\s+\"(\\w+)\".*$/\\1/m,module/",
    "--regex-LUA=/^\\s*module\\s+\"[a-zA-Z0-9._]+\\.(\\w+)\".*$/\\1/m,module/",
    "--languages=LUA",
    // "--regex-LUA=/^.*\\s*function\\s*(\\w+):(\\w+).*$/\\2/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*[0-9]+.*$/\\1/e/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\.(\\w+).*$/\\2/f/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\s*\\(.*$/\\1/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*\\{.*$/\\1/e/ --regex-LUA=/^\\s*module\\s+\"(\\w+)\".*$/\\1/m,module/ --regex-LUA=/^\\s*module\\s+\"[a-zA-Z0-9._]+\\.(\\w+)\".*$/\\1/m,module/ --excmd=number"
    // "--regex-LUA=/^.*\\s*function\\s*(\\w+):(\\w+).*$/\\2/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*[0-9]+.*$/\\1/e/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\.(\\w+).*$/\\2/f/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\s*\\(.*$/\\1/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*\\{.*$/\\1/e/ --regex-LUA=/^\\s*module\\s+\"(\\w+)\".*$/\\1/m,module/ --regex-LUA=/^\\s*module\\s+\"[a-zA-Z0-9._]+\\.(\\w+)\".*$/\\1/m,module/ --excmd=number"
    ],
    // "opts":[],
    // "opts" : "--langdef=LUA --langmap=LUA:.lua --regex-LUA=/^.*\\s*function\\s*(\\w+):(\\w+).*$/\\2/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*[0-9]+.*$/\\1/e/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\.(\\w+).*$/\\2/f/ --regex-LUA=/^.*\\s*function\\s*(\\w+)\\s*\\(.*$/\\1/f/ --regex-LUA=/^\\s*(\\w+)\\s*=\\s*\\{.*$/\\1/e/ --regex-LUA=/^\\s*module\\s+\"(\\w+)\".*$/\\1/m,module/ --regex-LUA=/^\\s*module\\s+\"[a-zA-Z0-9._]+\\.(\\w+)\".*$/\\1/m,module/ --languages=LUA",
    //
    "filters": {
        "source.python": {"type":"^i$"}
    },

    //
    "definition_filters": {
        "source.php": {"type":"^v$"}
    },

    //
    "definition_current_first": true,

    // Show the ctags menu in the context menus
    "show_context_menus": true,

    // Paths to additional tag files to include in tag search. This is a list
    // of items in the form [["language", "platform"], "path"]
    "extra_tag_paths": [[["source.python", "windows"], "C:\\Python27\\Lib\\tags"]],

    // Additional tag files to search
    "extra_tag_files": [".gemtags", "tags"],

    // Set to false so as not to select searched symbol (in Vintage mode)
    "select_searched_symbol": true
}

```

## 插件使用
1. 随便找到一个调用方法，鼠标右键，找到"navigate to definition",点击便可以跳转到对应的方法
2. 回到调用的地方，鼠标右键，点击"jump back"便可跳回方法

这样用鼠标来操作很是不方便，这是我们可以给CTags新增快捷键使用，或者快捷键配合鼠标使用
快捷键添加方法：
1. 点击"preferences"，依次找到"Package Settings"-> "Ctags" -> "Mouse Bindings-User"，点击打开文件
2. 添加如下代码保存即可，便实现了点击tab+鼠标左键调整的功能
```
[
    {
        "button": "button1",
        "count": 1,
        "press_command": "drag_select",
        "modifiers": ["ctrl"],
        "command": "navigate_to_definition"
    },
    {
        "button": "button2",
        "count": 1,
        "modifiers": ["ctrl"],
        "command": "jump_prev"
    }
]
```

