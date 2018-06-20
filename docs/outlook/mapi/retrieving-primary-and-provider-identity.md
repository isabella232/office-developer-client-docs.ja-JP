---
title: プライマリ デバイスとプロバイダーの Id を取得しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2a87e32fe21aa6fb1d9296c568a74da994c146bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803766"
---
# <a name="retrieving-primary-and-provider-identity"></a>プライマリ デバイスとプロバイダーの Id を取得しています。

  
  
**適用されます**: Outlook 
  
通常のアドレス帳プロバイダー、サービス ・ プロバイダーには、さまざまな状況でセッションを表すために使用できる id を指定するオプションがあります。 3 つのプロパティでは、プロバイダーの識別情報について説明します。
  
- **PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
これらのプロパティは、エントリ id、表示名、および対応する id のオブジェクトは、メッセージングのユーザーは、通常の検索キーに設定されます。 Id を提供するプロバイダーは、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティに STATUS_PRIMARY_IDENTITY フラグを設定します。
  
必要に応じて、セッションの特定のプロバイダーの id またはプライマリを使用する可能性があります。 表示のためにまたは**PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) などのプロパティを取得するためには、プロバイダーの id を使用します。 **PR_RESOURCE_PATH**場合、は、使用、またはプロバイダーによって作成されたファイルへのパスが含まれています。 セッションのユーザーに関連するファイルを検索する場合は、プライマリ id を提供するプロバイダーの**PR_RESOURCE_PATH**プロパティを取得します。 
  
 **特定のプロバイダーの id を取得するには**
  
1. ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 
    
2. [SPropertyRestriction](spropertyrestriction.md)構造体を使用して、指定されたプロバイダーの名前を**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) の列と一致する制約を作成します。 
    
3. プロバイダーの行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。 プロバイダーの識別情報は、存在する場合、[ **PR_IDENTITY_ENTRYID** ] 列で、保存されます。 
    
 **セッションのプライマリ id を取得するには**
  
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)を呼び出します。 **QueryIdentity**に基づいて、セッションの id、STATUS_PRIMARY_IDENTITY、 **PR_RESOURCE_FLAGS**の列の値の状態テーブル内の行のいずれかが存在します。 ステータス行の [なし] この値が設定されて、 **QueryIdentity**は 3 つの PR_IDENTITY プロパティを設定する最初のサービス プロバイダーの id を割り当てます。 サービス プロバイダーには、id が用意されていない、 **QueryIdentity**は MAPI_W_NO_SERVICE を返します。 このような場合、プライマリ id として使用できる汎用的なユーザーを表す文字列を作成する必要があります。 
    
 **セッションのプライマリ id を明示的に設定するには**
  
- [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)を呼び出します。 ターゲット ・ サービス ・ プロバイダーの**MAPIUID**を渡します。 
    

