---
title: 既定のプロファイルの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339313"
---
# <a name="setting-a-default-profile"></a>既定のプロファイルの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定のプロファイルは、 [MAPILogonEx](mapilogonex.md)への呼び出しで明示的に指定されていない場合に使用されるプロファイルです。 MAPI_USE_DEFAULT フラグの代わりに設定します。
  
 **既定のプロファイルを設定するには**
  
1. [MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。 
    
2. Call [IProfAdmin:: setdefaultprofile](iprofadmin-setdefaultprofile.md)。 **setdefaultprofile**は、新しい既定のプロファイルに対して**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティを設定し、以前の既定のプロファイルの設定を削除します。
    

