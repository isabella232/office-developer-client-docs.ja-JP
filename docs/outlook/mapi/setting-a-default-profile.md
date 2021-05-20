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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439815"
---
# <a name="setting-a-default-profile"></a>既定のプロファイルの設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定のプロファイルは [、MAPILogonEx](mapilogonex.md)の呼び出しで明示的に指定しない場合に使用されるプロファイルで、代わりに MAPI_USE_DEFAULT フラグを設定します。
  
 **既定のプロファイルを確立するには**
  
1. [MAPIAdminProfiles 関数を呼び出](mapiadminprofiles.md)して **、IProfAdmin** インターフェイス ポインターを取得します。 
    
2. [IProfAdmin::SetDefaultProfile を呼び出します](iprofadmin-setdefaultprofile.md)。 **SetDefaultProfile** は **PR_DEFAULT_PROFILE既定の** プロファイルの PR_DEFAULT_PROFILE ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティを設定し、以前の既定のプロファイルの設定を削除します。
    

