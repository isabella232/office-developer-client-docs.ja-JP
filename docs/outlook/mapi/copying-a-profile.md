---
title: プロファイルのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564935"
---
# <a name="copying-a-profile"></a>プロファイルのコピー

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイルを作成する方法の 1 つでは、既存のプロファイルからコピーし、必要なメッセージ サービスおよびサービス ・ プロバイダーを変更します。 プロファイルをコピーするには、 [MAPIAdminProfiles](mapiadminprofiles.md)関数によって、MAPI によって提供されるプロファイルの管理オブジェクトを使用する必要があります。 
  
 **プロファイルをコピーするには**
  
1. **IProfAdmin**インターフェイス ポインターを取得するために**MAPIAdminProfiles**を呼び出します。 
    
2. プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. コピーするプロファイルの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致する[SPropertyRestriction](spropertyrestriction.md)構造を持つプロパティの制限を作成します。 
    
4. プロファイル テーブルに適切な行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。 
    
5. [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)、 _lpszOldProfileName_パラメーターとして**PR_DISPLAY_NAME**列の値を渡すことを呼び出します。 
    

