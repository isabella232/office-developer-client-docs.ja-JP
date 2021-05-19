---
title: プロファイルのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424729"
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
    

