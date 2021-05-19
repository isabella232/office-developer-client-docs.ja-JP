---
title: Outlook プロファイルで Exchange Server のバージョンを検出する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424449"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Outlook プロファイルで Exchange Server のバージョンを検出する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックには **[、PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** プロパティと PR_PROFILE_SERVER_FULL_VERSION プロパティを使用して、アクティブ なアカウント **[](pidtagprofileserverfullversion-canonical-property.md)** が接続されている Microsoft Exchange Server のバージョン情報を取得する方法を示す C++ のコード サンプルが含まれています。 
  
コード  `GetProfileServiceVersion` サンプルの関数は、入力パラメーターとしてプロファイルを受け入れる。 指定したプロファイルに **PR_PROFILE_SERVER_VERSION** プロパティと **PR_PROFILE_SERVER_FULL_VERSION** プロパティが存在するかどうかに応じて、関数は各プロパティを取得し、適切なバージョン情報を出力パラメーターとして返します。 
  
`GetProfileServiceVersion` 最初に **[MAPIAdminProfiles 関数を呼び出](mapiadminprofiles.md)** してプロファイル管理オブジェクトを作成します。 次に、プロファイル管理オブジェクトを使用して **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** を呼び出して、メッセージ サービス管理オブジェクトを取得します。 メッセージ サービス管理オブジェクトを使用して **[、IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** を呼び出して現在のプロファイルのセクションを取得し **[、HrGetOneProp](hrgetoneprop.md)** を呼び出して、プロファイルのそのセクションに 2 つのプロパティがそれぞれ存在するかどうかを確認し、その場合は、適切な出力パラメーターにバージョン情報を設定します。 
  
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


