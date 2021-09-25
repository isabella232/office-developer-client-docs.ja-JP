---
title: 連絡先アドレス帳エントリを指定して連絡先メッセージを取得する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: '最終更新日: 2013 年 8 月 13 日'
ms.openlocfilehash: d4f56314dc8b2acac859f519ac2e15e219011b27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616972"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>連絡先アドレス帳エントリを指定して連絡先メッセージを取得する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、連絡先アドレス帳のエントリを識別する CONTAB_ENTRYID 構造を使用して、関連付けられた MAPI 連絡先メッセージを取得する方法を示す C++ の例 `HrOpenContact` を示します。 [](contab_entryid.md) 
  
`HrOpenContact` 次のパラメーターがあります。 
  
-  *lpSession は*  、現在のセッションを表す入力パラメーターです。 **LPMAPISESSION** は [、IMAPISession への](imapisessioniunknown.md)ポインターとして MAPI ヘッダー ファイル mapix.h で定義されています。
    
-  *cbEntryID は**、lpEntryID* に関連付けられたエントリ識別子のサイズを表す入力パラメーターです。 
    
-  *lpEntryID*  は、連絡先アドレス帳内のエントリのエントリ識別子へのポインターを表す入力パラメーターです。 
    
-  *ulFlags は*  、MAPI 連絡先メッセージへのオブジェクト アクセス フラグを含むビットマスクを表す入力パラメーターです。 
    
-  *lpContactMessage*  は、MAPI 連絡先メッセージへのポインターを表す出力パラメーターです。 
    
基になる MAPI 連絡先メッセージを開くには、 `HrOpenContact` 最初に *lpEntryID* をポインターにキャストCONTAB_ENTRYID。 その後 [、IMAPISession::OpenEntry](imapisession-openentry.md) を呼び出して MAPI 連絡先メッセージを取得し、MAPI 連絡先メッセージのエントリ識別子とエントリ識別子のサイズをそれぞれ識別する連絡先アドレス帳のエントリの  *cbeid*  フィールドと  *abeid*  フィールドをパラメーターとして渡します。 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
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
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
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

- [IMAPISession::OpenEntry](imapisession-openentry.md)

