---
title: 連絡先の連絡先アドレス帳のエントリを指定したメッセージを取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: '最終更新日: 2013 年 8 月 13 日'
ms.openlocfilehash: 346e6bc471f5257aacb34c2e7d02a0aade1bb46e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800241"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>連絡先の連絡先アドレス帳のエントリを指定したメッセージを取得します。

**適用対象**: Outlook 
  
このトピックには、C++ では、例が含まれている`HrOpenContact`、関連付けられている連絡先の MAPI メッセージを取得するのには、連絡先のアドレス帳のエントリを識別する[CONTAB_ENTRYID](contab_entryid.md)構造体を使用する方法を示します。 
  
`HrOpenContact`次のパラメーターがあります。 
  
-  *lpSession*は、現在のセッションを表す入力パラメーターです。 ポインターとして MAPI のヘッダー ファイル mapix.h に**LPMAPISESSION**が定義されている[IMAPISession: IUnknown](imapisessioniunknown.md)。
    
-  *cbEntryID*は、 *lpEntryID*に関連付けられたエントリ id のサイズを表す入力パラメーターです。 
    
-  *lpEntryID*は、連絡先のアドレス帳のエントリのエントリの識別子へのポインターを表す入力パラメーターです。 
    
-  *ulFlags*は、MAPI の連絡先のメッセージにオブジェクトのアクセス フラグを含むビットマスクを表す入力パラメーターです。 
    
-  *lpContactMessage*は、連絡先の MAPI メッセージへのポインターを表す出力パラメーターです。 
    
開くには、基になる MAPI 連絡先メッセージ`HrOpenContact` **CONTAB_ENTRYID**へのポインターへの*lpEntryID*を最初にキャストします。 *Cbeid*と*abeid*フィールドの連絡先アドレス帳のエントリのそれぞれのエントリ id のサイズを確認することをパラメーターとして渡す、連絡先の MAPI メッセージを取得する[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出して、連絡先の MAPI メッセージのエントリ id です。 
  
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

