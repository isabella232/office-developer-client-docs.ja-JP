---
title: TZDEFINITION 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 039b3a45-bd57-51f5-1485-a3f6d1bde85a
description: このトピックでは、バイナリのプロパティに格納されている永続化された形式からの TZDEFINITION 構造体を読み取る方法を示します。
ms.openlocfilehash: 1fdd4016d26c95cdbff80e88e34bdfac5aa91f06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799322"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzdefinition-structure"></a>TZDEFINITION 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。

このトピックでは、バイナリのプロパティに格納されている永続化された形式からの[TZDEFINITION](tzdefinition.md)構造体を読み取る方法を示します。 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &amp;lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &amp;gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &amp;gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp;amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &amp;lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp;amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &amp;lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &amp;lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &amp;lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```

## <a name="see-also"></a>関連項目

- [バイナリ プロパティをストリームに永続化の TZDEFINITION について](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)
