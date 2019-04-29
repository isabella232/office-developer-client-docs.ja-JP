---
title: Outlook プロファイルで Exchange Server のバージョンを検出する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424449"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a><span data-ttu-id="3701f-103">Outlook プロファイルで Exchange Server のバージョンを検出する</span><span class="sxs-lookup"><span data-stu-id="3701f-103">Detect the version of Exchange Server in an Outlook profile</span></span>

<span data-ttu-id="3701f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3701f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3701f-105">このトピックには、 **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** プロパティと**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** プロパティを使用して、アクティブなアカウントが Microsoft Exchange SERVER のバージョン情報を取得する方法を示す、C++ のコードサンプルが含まれています。に接続されています。</span><span class="sxs-lookup"><span data-stu-id="3701f-105">This topic includes a code sample in C++ that shows how to use the **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** property and **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** property to obtain version information of the Microsoft Exchange Server that the active account is connected to.</span></span> 
  
<span data-ttu-id="3701f-106">コード`GetProfileServiceVersion`サンプルの関数は、入力パラメーターとしてプロファイルを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="3701f-106">The  `GetProfileServiceVersion` function in the code sample accepts a profile as an input parameter.</span></span> <span data-ttu-id="3701f-107">**PR_PROFILE_SERVER_VERSION**プロパティと**PR_PROFILE_SERVER_FULL_VERSION**プロパティが指定されたプロファイルに存在するかどうかに応じて、関数は各プロパティを取得し、適切なバージョン情報を出力として返します。parameters.</span><span class="sxs-lookup"><span data-stu-id="3701f-107">Depending on whether the **PR_PROFILE_SERVER_VERSION** property and the **PR_PROFILE_SERVER_FULL_VERSION** property exist in the given profile, the function gets each property and returns the appropriate version information as output parameters.</span></span> 
  
<span data-ttu-id="3701f-108">`GetProfileServiceVersion`最初に**[MAPIAdminProfiles](mapiadminprofiles.md)** 関数を呼び出して、プロファイル管理オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3701f-108">`GetProfileServiceVersion` first calls the **[MAPIAdminProfiles](mapiadminprofiles.md)** function to create a profile administration object.</span></span> <span data-ttu-id="3701f-109">その後、プロファイル管理オブジェクトを使用して**[IProfAdmin:: adminservices](iprofadmin-adminservices.md)** を呼び出して、メッセージサービス管理オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3701f-109">It then uses the profile administration object to call **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** to obtain a message service administration object.</span></span> <span data-ttu-id="3701f-110">メッセージサービス管理オブジェクトを使用して、 **[IMsgServiceAdmin::](imsgserviceadmin-openprofilesection.md)** openprofilebyを呼び出して現在のプロファイルのセクションを取得した後、 **[hrgetoneprop](hrgetoneprop.md)** を呼び出して、次の2つのプロパティがそれぞれのセクションに存在するかどうかを確認します。プロファイルの場合は、該当する出力パラメーターにバージョン情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="3701f-110">Using the message service administration object, it calls **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** to obtain a section of the current profile, and then calls **[HrGetOneProp](hrgetoneprop.md)** to verify if each of the two properties exists in that section of the profile, and if so, sets the version information in the appropriate output parameters.</span></span> 
  
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


