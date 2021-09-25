---
title: 既定のプロファイルの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c7c28bcab989c778e98da6619bba6f8c628f7553
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586734"
---
# <a name="setting-a-default-profile"></a>既定のプロファイルの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定のプロファイルは [、MAPILogonEx](mapilogonex.md)の呼び出しで明示的に指定しない場合に使用されるプロファイルで、代わりに MAPI_USE_DEFAULT フラグを設定します。
  
 **既定のプロファイルを確立するには**
  
1. [MAPIAdminProfiles 関数を呼び出](mapiadminprofiles.md)して **、IProfAdmin** インターフェイス ポインターを取得します。 
    
2. [IProfAdmin::SetDefaultProfile を呼び出します](iprofadmin-setdefaultprofile.md)。 **SetDefaultProfile** は **PR_DEFAULT_PROFILE既定の** プロファイルの PR_DEFAULT_PROFILE ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティを設定し、以前の既定のプロファイルの設定を削除します。
    

