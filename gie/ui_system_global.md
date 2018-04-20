# 接口
`RegisterEvent(...)`
- 描述
  - RegisterEvent 注册事件，支持两种形式: RegisterEvent(szEvent, fnCallback, _anyCustomParams, _tScope) 与 RegisterEvent(uiobject, szEvent, fnCallback, _anyCustomParams, _tScope)

`UnRegisterEvent(szEvent, _tScope)`
- 描述
  - UnRegisterEvent 取消注册事件
- 参数
  - `szEvent` 事件名
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`RegisterActorEvent(actor, anyEvent, fnCallback, _anyCustomParams, _tScope)`
- 描述
  - RegisterActorEvent 注册角色事件
- 参数
  - `actor` 角色
  - `fnCallback` 回调，例：`funciton CallBack(anyEvent, tScope, anyCustomParams, actor, [...]) `
  - `_anyCustomParams` 自定义参数
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`UnRegisterActorEvent(actor, anyEvent, _tScope)`
- 描述
  - UnRegisterActorEvent 取消注册角色事件
- 参数
  - `actor` 角色
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`FireEvent(anyEvent, ...)`
- 描述
  - FireEvent 触发事件

`RegisterProperty(ACTOR_PROPERTY, fnCallback, _anyCustomParams, _tScope)`
- 描述
  - RegisterProperty 注册全局属性变化事件
- 参数
  - `ACTOR_PROPERTY` 属性枚举
  - `fnCallback` 回调，例：`funciton CallBack(ACTOR_PROPERTY, tScope, anyCustomParams, actor, szPropName, anyPropValue) `
  - `_anyCustomParams` 自定义参数
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`UnRegisterProperty(ACTOR_PROPERTY, _tScope)`
- 描述
  - UnRegisterProperty 取消注册全局属性变化事件
- 参数
  - `ACTOR_PROPERTY` 属性枚举
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`RegisterActorProperty(actor, ACTOR_PROPERTY, fnCallback, _anyCustomParams, _tScope)`
- 描述
  - RegisterActorProperty 注册指定的角色属性变化事件
- 参数
  - `actor` 角色
  - `ACTOR_PROPERTY` 属性枚举
  - `fnCallback` 回调，例：`funciton CallBack(ACTOR_PROPERTY, tScope, anyCustomParams, actor, szPropName, anyPropValue) `
  - `_anyCustomParams` 自定义参数
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`UnRegisterActorProperty(actor, ACTOR_PROPERTY, _tScope)`
- 描述
  - UnRegisterActorProperty 取消注册指定的角色属性变化事件
- 参数
  - `actor` 角色
  - `ACTOR_PROPERTY` 属性枚举
  - `_tScope` 将事件注册到指定的域，默认域为当前插件

`SetTimer(szName, fIntervalMS, fnCallback, ...)`
- 描述
  - SetTimer 注册持续触发的定时器
- 参数
  - `szName` 定时器名，可为nil
  - `fIntervalMS` 定时器触发间隔时间，毫秒
  - `fnCallback` 回调，例：`funciton CallBack(szTimerName, ...) ` 

`SetDelayTimer(szName, fDelayTimeMS, fnCallback, ...)`
- 描述
  - SetDelayTimer 注册触发一次的定时器
- 参数
  - `szName` 定时器名，可为nil
  - `fDelayTimeMS` 定时器触发时间，毫秒
  - `fnCallback` 回调，例：`funciton CallBack(szTimerName, ...) ` 

`KillTimer(szName)`
- 描述
  - KillTimer 取消定时器
- 参数
  - `szName` 定时器名

`SetPos(pos, _fX, _fY, _fZ, _fYaw)`
- 描述
  - SetPos 增量修改pos对象，_fX, _fY, _fZ, _fYaw 4参数会覆盖当前值，nil为不修改
- 参数
  - `pos` 要覆盖修改的pos对象
  - `_fX` x 坐标
  - `_fY` y 坐标
  - `_fZ` z 坐标
  - `_fYaw` 朝向信息

`ModifyPos(pos, _fX, _fY, _fZ, _fYaw)`
- 描述
  - SetPos 增量修改pos对象，_fX, _fY, _fZ, _fYaw 4参数会+到当前值上，nil为不修改
- 参数
  - `pos` 要覆盖修改的pos对象
  - `_fX` x 坐标
  - `_fY` y 坐标
  - `_fZ` z 坐标
  - `_fYaw` 朝向信息

`ReleasePos(pos)`
- 描述
  - ReleasePos 释放pos，当确认一个pos对象完全不需要使用时，可释放该pos优化代码（慎重使用）
- 参数
  - `pos` 要释放的pos对象

`GetScene()`
- 描述
  - GetScene 获取当前客户端的场景

`player = GetLocalPlayer()`
- 描述
  - GetLocalPlayer 获取当前客户端的本地玩家

