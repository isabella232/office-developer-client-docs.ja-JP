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
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="104e3-103">連絡先アドレス帳エントリが指定された連絡先メッセージを取得する</span><span class="sxs-lookup"><span data-stu-id="104e3-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="104e3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="104e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="104e3-105">このトピックには、C++ `HrOpenContact`の例が含まれています。これは、連絡先アドレス帳のエントリを識別する[CONTAB_ENTRYID](contab_entryid.md)構造を使用して、関連付けられている MAPI 連絡先メッセージを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="104e3-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="104e3-106">`HrOpenContact`には、次のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="104e3-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="104e3-107">*lpsession*は、現在のセッションを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="104e3-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="104e3-108">**LPMAPISESSION**は、MAPI ヘッダーファイルマップ ix で、 [imapisession: IUnknown](imapisessioniunknown.md)へのポインターとして定義されています。</span><span class="sxs-lookup"><span data-stu-id="104e3-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="104e3-109">*cbEntryID*は、 *l tryid*に関連付けられたエントリ識別子のサイズを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="104e3-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="104e3-110">*lな tryid*は、連絡先アドレス帳のエントリのエントリ id へのポインターを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="104e3-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="104e3-111">*ulflags*は、MAPI 連絡先メッセージへのオブジェクトアクセスフラグを含むビットマスクを表す入力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="104e3-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="104e3-112">*lpcontactmessage*は、MAPI 連絡先メッセージへのポインターを表す出力パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="104e3-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="104e3-113">基になる MAPI 連絡先メッセージを開く`HrOpenContact`には、最初に*lCONTAB_ENTRYID tryid*を\*\*\*\* へのポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="104e3-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="104e3-114">次に、 [imapisession:: openentry](imapisession-openentry.md)を呼び出して、MAPI の連絡先メッセージを取得します。パラメーターとして、連絡先アドレス帳のエントリの*cbeid*と*abeid*フィールドを渡します。それぞれの値は、エントリ id のサイズとMAPI 連絡先メッセージのエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="104e3-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="104e3-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="104e3-115">See also</span></span>

- [<span data-ttu-id="104e3-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="104e3-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)

