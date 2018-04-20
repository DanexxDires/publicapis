# 说明
- 这是一个字典文件 Demo

# 属性
---
`fPi = math.pi`
---
- 描述
  - π

# 接口
---
`anyValue                       = assert              (anyValue, _szMessage)`
`_                              = error               (_szMessage, _nLevel)`
`dwIndex, anyValue              = ipairs              (tTable)`
`anyValue                       = next                (tTable, _dwIndex)`
`anyKey, anyValue               = pairs               (tTable)`
`...                            = pcall               (fnFunc, ...)`
`_                              = print               (...)`
`nNumber                        = tonumber            (anyValue, _dwBase)`
`szString                       = tostring            (anyValue)`
`szType                         = type                (anyValue)`
`tTargetTable                   = setmetatable        (tTargetTable, tMetatable)`
`tMetatable                     = getmetatable        (anyObject)`

`...                            = string.byte         (szString, _dwStartIndex, _dwEndIndex)`
`...                            = string.char         (...)`
`dwStartIndex, dwEndIndex, ...  = string.find         (szString, szPattern, _dwStartIndex, _bPlain)`
`szFormatedString               = string.format       (szString, ...)`
`...                            = string.gmatch       (szString, szPattern)`
`szResultString                 = string.gsub         (szString, anyPattern, szReplaceString, _dwNumber)`
`dwLength                       = string.len          (szString)`
`szLowerString                  = string.lower        (szString)`
`szMatchedString                = string.match        (szString, szPattern, _dwStartIndex)`
`szResultString                 = string.rep          (szString, dwRepeatTimes, _szSeparator)`
`szReversedString               = string.reverse      (szString)`
`szSubstring                    = string.sub          (szString, dwStartIndex, _dwEndIndex)`
`szUpperString                  = string.upper        (szString)`
`bIsEmpty                       = string.isempty      (szString)`
`tSplitedList                   = string.split        (szString, anySpliter, _bRemoveEmptyEntries, _tResult)`
`szFormatPattern                = string.gformat      (szFormatPattern, ...)`

`...                            = sz:byte             (_dwStartIndex, _dwEndIndex)`
`dwStartIndex, dwEndIndex, ...  = sz:find             (szPattern, _dwStartIndex, _bPlain)`
`szFormatedString               = sz:format           (...)`
`...                            = sz:gmatch           (szPattern)`
`szResultString                 = sz:gsub             (anyPattern, szReplaceString, _dwNumber)`
`dwLength                       = sz:len              ()`
`szLowerString                  = sz:lower            ()`
`szMatchedString                = sz:match            (szPattern, _dwStartIndex)`
`szResultString                 = sz:rep              (dwRepeatTimes, _szSeparator)`
`szReversedString               = sz:reverse          ()`
`szSubstring                    = sz:sub              (dwStartIndex, _dwEndIndex)`
`szUpperString                  = sz:upper            ()`
`bIsEmpty                       = sz:isempty          ()`
`tSplitedList                   = sz:split            (anySpliter, _bRemoveEmptyEntries, _tResult)`
`szFormatPattern                = sz:gformat          (...)`

`szConcatedString               = table.concat        (tTable, _szSeparator, _dwStartIndex, _dwEndIndex)`
`tTable                         = table.insert        (tTable, anyInsertIndexOrValue, _anyValue)`
`tPackingTable                  = table.pack          (...)`
`tTable                         = table.remove        (tTable, _dwRemoveIndex)`
`tTable                         = table.sort          (tTable, _fnComparer)`
`...                            = table.unpack        (tTable, _dwStartIndex, _dwEndIndex)`
`tTable                         = table.reset         (tTable)`

`nAbsoluteNumber                = math.abs            (nNumber)`
`nAcosRadian                    = math.acos           (nX)`
`nAsinRadian                    = math.asin           (nX)`
`nAtanRadian                    = math.atan           (nY, _nX)`
`dwCeilInteger                  = math.ceil           (nNumber)`
`nCosValue                      = math.cos            (nRadian)`
`nAngle                         = math.deg            (nRadian)`
`dwFloorInteger                 = math.floor          (nNumber)`
`nRemainder                     = math.fmod           (nDividend, nDivisor)`
`fHugeValue                     = math.huge           ()`
`nMaxNumber                     = math.max            (nNumber, ...)`
`nMaxInteger                    = math.maxinteger     ()`
`nMinNumber                     = math.min            (nNumber, ...)`
`nMinInteger                    = math.mininteger     ()`
`nIntegralPart, fFloatPart      = math.modf           (nNumber)`
`nRadian                        = math.rad            (nAngle)`
`nRandomValue                   = math.random         (_nMinValue, _nMaxValue)`
`_                              = math.randomseed     (nSeed)`
`nSinValue                      = math.sin            (nRadian)`
`nSquareRoot                    = math.sqrt           (nNumber)`
`nTanValue                      = math.tan            (nRadian)`
`nInteger                       = math.tointeger      (anySource)`
`szType                         = math.type           (anySource)`
`nNumber                        = math.clamp          (nValue, nMin, nMax)`
`nNumber                        = math.lerp           (nValueA, nValueB, fPercent, fExponent)`
`nInteger                       = math.round          (nValue)`

`bBitState = math.getbit(qwData, nBitIndex, _bDebugInfo)`
---
- 描述
  - 获取一个64位整数的指定位的状态
- 参数
  - `qwData` 待获取位信息的源数据
  - `nBitIndex` 待获取状态的位, 需要注意的是位是从 0 开始的, 上限为 63
  - `_bDebugInfo` 是否打印调试信息(按位显示的二进制字符串信息)
- 返回
  - `bBitState` 指定位的状态, 为 true 或 false

`qwNewData = math.setbit(qwData, nBitIndex, bBitState, _bDebugInfo)`
---
- 描述
  - 设置一个64位整数的指定位的状态
- 参数
  - `qwData` 待设置位信息的源数据
  - `nBitIndex` 待设置状态的位, 需要注意的是位是从 0 开始的, 上限为 63
  - `bBitState` 待设置状态的值, true 时将位指定设置为 1, false 时将指定位设置为 0
  - `_bDebugInfo` 是否打印调试信息(按位显示的二进制字符串信息)
- 返回
  - `qwNewData` 设置位信息后的数据(64位整数)

`bApproximately = math.approximate(anyV1, anyV2, _fPrecision)`
---
- 描述
  - 判断两个值是否近似相等, 如判断两个浮点数是否近似相等
- 参数
  - `anyV1` 参与比较的值1
  - `anyV2` 参与比较的值2
  - `_fPrecision` 判断精度, 默认为 0.00001
- 返回
  - `bApproximately` 两个值是否近似相等
