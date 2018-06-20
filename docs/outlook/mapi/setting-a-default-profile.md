---
title: 既定のプロファイルを設定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803880"
---
# <a name="setting-a-default-profile"></a>既定のプロファイルを設定します。

  
  
**適用されます**: Outlook 
  
既定のプロファイルは、明示的に指定しない[MAPILogonEx](mapilogonex.md)、MAPI_USE_DEFAULT フラグを設定する代わりに呼び出しのいずれかの場合に使用されるプロファイルです。
  
 **既定のプロファイルを確立するために**
  
1. **IProfAdmin**インターフェイス ポインターを取得するために[MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出します。 
    
2. [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)を呼び出します。 **SetDefaultProfile**は、新しい既定のプロファイルで、 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) のプロパティを設定し、以前の既定のプロファイルの設定を削除します。
    

