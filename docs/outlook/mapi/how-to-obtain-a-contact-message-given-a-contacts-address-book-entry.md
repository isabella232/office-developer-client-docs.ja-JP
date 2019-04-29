---
title: 連絡先アドレス帳エントリが指定された連絡先メッセージを取得する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: '最終更新日: 2013 年8月13日'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437792"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>連絡先アドレス帳エントリが指定された連絡先メッセージを取得する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックには、C++ `HrOpenContact`の例が含まれています。これは、連絡先アドレス帳のエントリを識別する[CONTAB_ENTRYID](contab_entryid.md)構造を使用して、関連付けられている MAPI 連絡先メッセージを取得する方法を示しています。 
  
`HrOpenContact`には、次のパラメーターがあります。 
  
-  *lpsession*は、現在のセッションを表す入力パラメーターです。 **LPMAPISESSION**は、MAPI ヘッダーファイルマップ ix で、 [imapisession: IUnknown](imapisessioniunknown.md)へのポインターとして定義されています。
    
-  *cbEntryID*は、 *l tryid*に関連付けられたエントリ識別子のサイズを表す入力パラメーターです。 
    
-  *lな tryid*は、連絡先アドレス帳のエントリのエントリ id へのポインターを表す入力パラメーターです。 
    
-  *ulflags*は、MAPI 連絡先メッセージへのオブジェクトアクセスフラグを含むビットマスクを表す入力パラメーターです。 
    
-  *lpcontactmessage*は、MAPI 連絡先メッセージへのポインターを表す出力パラメーターです。 
    
基になる MAPI 連絡先メッセージを開く`HrOpenContact`には、最初に*lCONTAB_ENTRYID tryid*を**** へのポインターにキャストします。 次に、 [imapisession:: openentry](imapisession-openentry.md)を呼び出して、MAPI の連絡先メッセージを取得します。パラメーターとして、連絡先アドレス帳のエントリの*cbeid*と*abeid*フィールドを渡します。それぞれの値は、エントリ id のサイズとMAPI 連絡先メッセージのエントリ識別子。 
  
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

