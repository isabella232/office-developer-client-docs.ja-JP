---
title: Outlook プロファイルに Exchange Server のバージョンを検出します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: b6c1482554cfb1e756266eb31f992b81bc34bb51
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575897"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Outlook プロファイルに Exchange Server のバージョンを検出します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
このトピックには、アクティブなアカウントが Microsoft Exchange Server のバージョン情報を取得するのには、 **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** プロパティと**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** プロパティを使用する方法について説明する C++ のコード サンプルが含まれています接続されています。 
  
`GetProfileServiceVersion`のコード サンプルでは関数は、入力パラメーターとしてプロファイルを受け取ります。 によってかどうか、 **PR_PROFILE_SERVER_VERSION**プロパティと**PR_PROFILE_SERVER_FULL_VERSION**プロパティは、特定のプロファイルに存在、関数が各プロパティを取得し、出力として適切なバージョン情報を返します。パラメーターです。 
  
`GetProfileServiceVersion`最初のプロファイルの管理オブジェクトを作成する**[MAPIAdminProfiles](mapiadminprofiles.md)** 関数を呼び出します。 プロファイルの管理オブジェクトを使用して、メッセージ サービスの管理オブジェクトを取得するのには**[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** を呼び出します。 メッセージ サービスの管理オブジェクトを使用すると、現在のプロファイルのセクションを取得する**[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** を呼び出すの特定のセクションに存在するかどうかの 2 つのプロパティを確認するのには、 **[HrGetOneProp](hrgetoneprop.md)** を呼び出して、プロファイル、および場合は、適切な出力パラメーターのバージョン情報を設定します。 
  
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


