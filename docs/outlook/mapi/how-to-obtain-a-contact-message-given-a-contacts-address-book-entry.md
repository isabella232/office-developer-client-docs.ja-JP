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
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="6d261-103">連絡先の連絡先アドレス帳のエントリを指定したメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="6d261-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="6d261-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d261-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d261-105">このトピックには、C++ では、例が含まれている`HrOpenContact`、関連付けられている連絡先の MAPI メッセージを取得するのには、連絡先のアドレス帳のエントリを識別する[CONTAB_ENTRYID](contab_entryid.md)構造体を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6d261-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="6d261-106">`HrOpenContact`次のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="6d261-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="6d261-107">*lpSession*は、現在のセッションを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="6d261-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="6d261-108">ポインターとして MAPI のヘッダー ファイル mapix.h に**LPMAPISESSION**が定義されている[IMAPISession: IUnknown](imapisessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="6d261-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="6d261-109">*cbEntryID*は、 *lpEntryID*に関連付けられたエントリ id のサイズを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="6d261-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="6d261-110">*lpEntryID*は、連絡先のアドレス帳のエントリのエントリの識別子へのポインターを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="6d261-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="6d261-111">*ulFlags*は、MAPI の連絡先のメッセージにオブジェクトのアクセス フラグを含むビットマスクを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="6d261-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="6d261-112">*lpContactMessage*は、連絡先の MAPI メッセージへのポインターを表す出力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="6d261-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="6d261-113">開くには、基になる MAPI 連絡先メッセージ`HrOpenContact` **CONTAB_ENTRYID**へのポインターへの*lpEntryID*を最初にキャストします。</span><span class="sxs-lookup"><span data-stu-id="6d261-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="6d261-114">*Cbeid*と*abeid*フィールドの連絡先アドレス帳のエントリのそれぞれのエントリ id のサイズを確認することをパラメーターとして渡す、連絡先の MAPI メッセージを取得する[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出して、連絡先の MAPI メッセージのエントリ id です。</span><span class="sxs-lookup"><span data-stu-id="6d261-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="6d261-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d261-115">See also</span></span>

- [<span data-ttu-id="6d261-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6d261-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)

