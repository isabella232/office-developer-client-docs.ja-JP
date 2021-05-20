---
title: プライマリ ID とプロバイダー ID の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430813"
---
# <a name="retrieving-primary-and-provider-identity"></a>プライマリ ID とプロバイダー ID の取得

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダー (通常はアドレス帳プロバイダー) には、さまざまな状況でセッションを表す ID を指定できます。 3 つのプロパティは、プロバイダーの ID を表します。
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
これらのプロパティは、対応する ID オブジェクトのエントリ識別子、表示名、および検索キー (通常はメッセージング ユーザー) に設定されます。 ID を指定するプロバイダーは、STATUS_PRIMARY_IDENTITY **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティPR_RESOURCE_FLAGSフラグも設定します。
  
ニーズに応じて、特定のプロバイダーの ID またはセッションのプライマリ ID を使用できます。 プロバイダーの ID は、表示またはプロパティの取得にも使用できます (たとえば、PR_RESOURCE_PATH  [(PidTagResourcePath)。](pidtagresourcepath-canonical-property.md) **PR_RESOURCE_PATH** 設定されている場合は、プロバイダーによって使用または作成されたファイルへのパスが含まれる。 セッションの **PR_RESOURCE_PATH** に関連するファイルを検索する場合に、プライマリ ID を指定するプロバイダーの PR_RESOURCE_PATH プロパティを取得します。 
  
 **特定のプロバイダーの ID を取得するには**
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。 
    
2. [SPropertyRestriction](spropertyrestriction.md)構造体を使用して制限を作成し **、PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) 列と指定したプロバイダーの名前を一致します。 
    
3. [IMAPITable::FindRow を呼び出して](imapitable-findrow.md)、プロバイダーの行を探します。 プロバイダーの ID は、存在する場合 **、PR_IDENTITY_ENTRYID列に** 格納されます。 
    
 **セッションのプライマリ ID を取得するには**
  
- [IMAPISession::QueryIdentity を呼び出します](imapisession-queryidentity.md)。 **QueryIdentity は**、状態テーブルのいずれかの行の STATUS_PRIMARY_IDENTITY 列に PR_RESOURCE_FLAGS値が存在する場合にセッション ID を基にします。 どの状態行にもこの値が設定されている場合 **、QueryIdentity** は、3 つのプロパティを設定する最初のサービス プロバイダーに id をPR_IDENTITYします。 ID を提供するサービス プロバイダーがない場合 **、QueryIdentity** は id をMAPI_W_NO_SERVICE。 この場合は、プライマリ ID として機能できる汎用ユーザーを表す文字列を作成する必要があります。 
    
 **セッションのプライマリ ID を明示的に設定するには**
  
- [IMsgServiceAdmin::SetPrimaryIdentity を呼び出します](imsgserviceadmin-setprimaryidentity.md)。 ターゲット サービス **プロバイダーの MAPIUID** を渡します。 
    

