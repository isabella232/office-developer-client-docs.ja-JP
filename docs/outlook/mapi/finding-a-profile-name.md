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
  
クライアントは、セッションで現在使用されているプロファイルの名前、既定のプロファイルの名前、またはコンピューターにインストールされている代替プロファイルの名前を検索する必要がある場合があります。
  
セッション中にプロファイルの名前を取得するには、いくつかの方法があります。 セッションで使用されているものとは限らないプロファイルの名前を検索する必要がある場合は、最初の手順を使用します。 既定のプロファイルの名前を検索する必要がある場合は、2番目の手順を使用します。 セッションの現在のプロファイルの名前を検索する必要がある場合は、last プロシージャを使用します。 
  
 **任意のプロファイルの名前を検索するには**
  
1. [MAPIAdminProfiles](mapiadminprofiles.md)を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。 
    
2. プロファイルテーブルにアクセスするには、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. プロファイルテーブルの[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出して、テーブル内のすべての行を取得し、それぞれの行を調べてターゲットプロファイルを表しているかどうかを確認します。 
    
 **既定のプロファイルの名前を検索するには**
  
1. [MAPIAdminProfiles](mapiadminprofiles.md)を呼び出します。
    
2. プロファイルテーブルにアクセスするには、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) と値が TRUE に一致する[spropertyrestriction](spropertyrestriction.md)構造を持つプロパティ制限を構築します。
    
4. [ [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して、既定のプロファイルを表すプロファイルテーブルの行を検索します。 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 列には、既定のプロファイルの名前が含まれています。
    
 **現在のプロファイルの名前を検索するには**
  
現在のプロファイルの名前を検索するには、次のいずれかの手順を実行します。
  
- 現在のプロファイルのセクションの1つを表す[MAPIUID](mapiuid.md)構造体がある場合は、 _lpuid_パラメーターにそのセクションを渡して[imapisession:: openprofile](imapisession-openprofilesection.md)のセクションに渡します。 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して、プロファイルセクションの**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティを取得します。 
    
- 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスして、その**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列が MAPI_SUBSYSTEM に設定されている行を検索します。 この行の**PR_DISPLAY_NAME**列はプロファイル名です。 起動時に状態テーブルを使用しないでください。これは、MAPI スプーラーがすべてのトランスポートプロバイダーの初期化を終了するまでアプリケーションをブロックするためです。 これにより、パフォーマンスが低下する可能性があります。 
    

