---
title: プロファイル名の検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800059"
---
# <a name="finding-a-profile-name"></a>プロファイル名の検索

  
  
**適用対象**: Outlook 
  
クライアントは、セッション、既定のプロファイルの名前、またはコンピューターにインストールされている別のプロファイルの名前を現在使用されているプロファイルの名前を検索する必要があります。
  
セッションの実行中にプロファイルの名前を取得するためにいくつかの方法があります。 必ずしも 1 つのセッションで使用されているプロファイルの名前を検索する場合は、最初の手順を使用します。 既定のプロファイルの名前を検索する場合は、2 番目の手順を使用します。 セッションの現在のプロファイルの名前を検索する場合は、最後の手順を使用します。 
  
 **任意のプロファイルの名前を検索するには**
  
1. **IProfAdmin**インターフェイス ポインターを取得するために[MAPIAdminProfiles](mapiadminprofiles.md)を呼び出します。 
    
2. プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. プロファイル テーブルの[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出して、テーブル内の行のすべてを取得し、ターゲット ・ プロファイルを表すかどうかを確認するには、各 1 を調べる。 
    
 **デフォルトのプロファイルの名前を検索するには**
  
1. [MAPIAdminProfiles](mapiadminprofiles.md)を呼び出します。
    
2. プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. TRUE の値を持つ**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) に一致する[SPropertyRestriction](spropertyrestriction.md)構造を持つプロパティの制限を作成します。
    
4. 既定のプロファイルを表すプロファイル テーブルの行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 列には、既定のプロファイルの名前が含まれています。
    
 **現在のプロファイルの名前を検索するには**
  
現在のプロファイルの名前を検索するには、次の手順のいずれかを行います。
  
- 現在のプロファイルのセクションのいずれかを表す[MAPIUID](mapiuid.md)の構造体がある場合は、 [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)に_lpUID_パラメーターで渡すことです。 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用してプロファイル セクションの**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) のプロパティを取得します。 
    
- ステータス テーブルにアクセスし、MAPI_SUBSYSTEM に設定されて、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) の列を持つ行を見つけるには、 [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 この行の**PR_DISPLAY_NAME**列は、プロファイルの名前です。 使用されないステータス テーブル開始時にすべてのトランスポート プロバイダーを初期化して、MAPI スプーラーが終了するまでアプリケーションをブロックするためです。 これによって、パフォーマンスが低下します。 
    

