---
title: Outlook プロファイルに Exchange Server のバージョンを検出します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 3ed3def3fd76ec4f67239958b5d5164d97f81d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800218"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a><span data-ttu-id="8c751-103">Outlook プロファイルに Exchange Server のバージョンを検出します。</span><span class="sxs-lookup"><span data-stu-id="8c751-103">Detect the version of Exchange Server in an Outlook profile</span></span>

<span data-ttu-id="8c751-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c751-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c751-105">このトピックには、アクティブなアカウントが Microsoft Exchange Server のバージョン情報を取得するのには、 **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** プロパティと**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** プロパティを使用する方法について説明する C++ のコード サンプルが含まれています接続されています。</span><span class="sxs-lookup"><span data-stu-id="8c751-105">This topic includes a code sample in C++ that shows how to use the **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** property and **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** property to obtain version information of the Microsoft Exchange Server that the active account is connected to.</span></span> 
  
<span data-ttu-id="8c751-106">`GetProfileServiceVersion`のコード サンプルでは関数は、入力パラメーターとしてプロファイルを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8c751-106">The  `GetProfileServiceVersion` function in the code sample accepts a profile as an input parameter.</span></span> <span data-ttu-id="8c751-107">によってかどうか、 **PR_PROFILE_SERVER_VERSION**プロパティと**PR_PROFILE_SERVER_FULL_VERSION**プロパティは、特定のプロファイルに存在、関数が各プロパティを取得し、出力として適切なバージョン情報を返します。パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="8c751-107">Depending on whether the **PR_PROFILE_SERVER_VERSION** property and the **PR_PROFILE_SERVER_FULL_VERSION** property exist in the given profile, the function gets each property and returns the appropriate version information as output parameters.</span></span> 
  
<span data-ttu-id="8c751-108">`GetProfileServiceVersion`最初のプロファイルの管理オブジェクトを作成する**[MAPIAdminProfiles](mapiadminprofiles.md)** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8c751-108">`GetProfileServiceVersion` first calls the **[MAPIAdminProfiles](mapiadminprofiles.md)** function to create a profile administration object.</span></span> <span data-ttu-id="8c751-109">プロファイルの管理オブジェクトを使用して、メッセージ サービスの管理オブジェクトを取得するのには**[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8c751-109">It then uses the profile administration object to call **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** to obtain a message service administration object.</span></span> <span data-ttu-id="8c751-110">メッセージ サービスの管理オブジェクトを使用すると、現在のプロファイルのセクションを取得する**[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** を呼び出すの特定のセクションに存在するかどうかの 2 つのプロパティを確認するのには、 **[HrGetOneProp](hrgetoneprop.md)** を呼び出して、プロファイル、および場合は、適切な出力パラメーターのバージョン情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="8c751-110">Using the message service administration object, it calls **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** to obtain a section of the current profile, and then calls **[HrGetOneProp](hrgetoneprop.md)** to verify if each of the two properties exists in that section of the profile, and if so, sets the version information in the appropriate output parameters.</span></span> 
  
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


