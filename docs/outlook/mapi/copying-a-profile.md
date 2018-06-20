---
title: プロファイルをコピーします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 77c7853c07830804aaa044f08078d95785bcfda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799827"
---
# <a name="copying-a-profile"></a>プロファイルをコピーします。

  
  
**適用されます**: Outlook 
  
プロファイルを作成する方法の 1 つでは、既存のプロファイルからコピーし、必要なメッセージ サービスおよびサービス ・ プロバイダーを変更します。 プロファイルをコピーするには、 [MAPIAdminProfiles](mapiadminprofiles.md)関数によって、MAPI によって提供されるプロファイルの管理オブジェクトを使用する必要があります。 
  
 **プロファイルをコピーするには**
  
1. **IProfAdmin**インターフェイス ポインターを取得するために**MAPIAdminProfiles**を呼び出します。 
    
2. プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. コピーするプロファイルの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致する[SPropertyRestriction](spropertyrestriction.md)構造を持つプロパティの制限を作成します。 
    
4. プロファイル テーブルに適切な行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。 
    
5. [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)、 _lpszOldProfileName_パラメーターとして**PR_DISPLAY_NAME**列の値を渡すことを呼び出します。 
    

