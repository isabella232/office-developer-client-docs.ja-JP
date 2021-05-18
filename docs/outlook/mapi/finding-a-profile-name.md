---
title: プロファイル名の検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407922"
---
# <a name="finding-a-profile-name"></a>プロファイル名の検索

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、セッションに現在使用されているプロファイルの名前、既定のプロファイルの名前、またはコンピューターにインストールされている代替プロファイルの名前を見つける必要がある場合があります。
  
セッション中にプロファイルの名前を取得するには、いくつかの方法があります。 セッションで必ずしも使用されていないプロファイルの名前を見つける必要がある場合は、最初の手順を使用します。 既定のプロファイルの名前を見つける必要がある場合は、2 番目の手順を使用します。 セッションの現在のプロファイルの名前を見つける必要がある場合は、最後の手順を使用します。 
  
 **プロファイルの名前を見つけるには**
  
1. [MAPIAdminProfiles を呼び出](mapiadminprofiles.md)して **、IProfAdmin インターフェイス ポインターを** 取得します。 
    
2. [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出して、プロファイル テーブルにアクセスします。 
    
3. プロファイル テーブルの [IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを呼び出して、テーブル内のすべての行を取得し、各行を調べて、ターゲット プロファイルを表すかどうかを判断します。 
    
 **既定のプロファイルの名前を見つけるには**
  
1. [MAPIAdminProfiles を呼び出します](mapiadminprofiles.md)。
    
2. [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出して、プロファイル テーブルにアクセスします。 
    
3. [SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築し、PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) と値 TRUE を一致します。
    
4. [IMAPITable::FindRow を](imapitable-findrow.md)呼び出して、既定のプロファイルを表すプロファイル テーブル内の行を検索します。 **[PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)列には、既定のプロファイルの名前が含まれる。
    
 **現在のプロファイルの名前を見つけるには**
  
現在のプロファイルの名前を見つけるには、次のいずれかの手順を実行します。
  
- 現在のプロファイルのセクションの 1 つを表す [MAPIUID](mapiuid.md) 構造がある場合は  _、lpUID_ パラメーターで [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)に渡します。 IMAPIProp::GetProps メソッドを **PR_PROFILE_NAME** プロファイル セクションのプロパティ [(PidTagProfileName)](pidtagprofilename-canonical-property.md)[プロパティを取得](imapiprop-getprops.md)します。 
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスし **、PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列が MAPI_SUBSYSTEM に設定されている行を検索します。 この **PR_DISPLAY_NAME** の列はプロファイル名です。 MAPI スプーラーがすべてのトランスポート プロバイダーの初期化を完了するまで、アプリケーションをブロックするために、起動中に状態テーブルを使用しない。 これにより、パフォーマンスが低下する可能性があります。 
    

