---
title: プロファイルのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4bf3bd7c5d509b0464a620ad0e8a6c00d45b9874
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611001"
---
# <a name="copying-a-profile"></a>プロファイルのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルを作成する 1 つの方法は、既存のプロファイルからコピーし、必要なメッセージ サービスとサービス プロバイダーを変更する方法です。 プロファイルのコピーには [、MAPIAdminProfiles](mapiadminprofiles.md) 関数を介して MAPI によって提供されるプロファイル管理オブジェクトを使用する必要があります。 
  
 **プロファイルをコピーするには**
  
1. **MAPIAdminProfiles を呼び出** して **、IProfAdmin インターフェイス ポインターを** 取得します。 
    
2. [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出して、プロファイル テーブルにアクセスします。 
    
3. [SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を作成し **、PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) とコピーするプロファイルの名前を一致します。 
    
4. [IMAPITable::FindRow を呼び出](imapitable-findrow.md)して、プロファイル テーブル内の適切な行を探します。 
    
5. [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)を呼び出し、PR_DISPLAY_NAMEの値を _lpszOldProfileName パラメーターとして渡_ します。  
    

