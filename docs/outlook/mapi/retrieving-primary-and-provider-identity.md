---
title: プライマリとプロバイダー id の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328638"
---
# <a name="retrieving-primary-and-provider-identity"></a>プライマリとプロバイダー id の取得

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダー (通常はアドレス帳プロバイダー) は、さまざまな状況でセッションを表すために使用できる id を提供するオプションを備えています。 次の3つのプロパティは、プロバイダーの id を記述します。
  
- **PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
これらのプロパティは、主にメッセージングユーザーである、対応する identity オブジェクトのエントリ id、表示名、および検索キーに設定されます。 id を指定するプロバイダーも、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに STATUS_PRIMARY_IDENTITY フラグを設定します。
  
必要に応じて、特定のプロバイダーの id またはセッションのプライマリ id を使用することができます。 プロバイダーの id を使用して、表示を目的にしたり、 **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) などのプロパティを取得したりすることもできます。 **PR_RESOURCE_PATH**(設定されている場合) は、プロバイダーによって使用または作成されたファイルへのパスを含みます。 セッションのユーザーに関連するファイルを検索する場合は、プライマリ id を提供するプロバイダーの**PR_RESOURCE_PATH**プロパティを取得します。 
  
 **特定のプロバイダーの id を取得するには**
  
1. 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。 
    
2. [spropertyrestriction](spropertyrestriction.md)構造を使用して制限を構築し、 **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) 列と指定されたプロバイダーの名前を照合します。 
    
3. $ [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して、プロバイダーの行を見つけます。 プロバイダーの id は、 **PR_IDENTITY_ENTRYID**列が存在する場合は、その列に格納されます。 
    
 **セッションのプライマリ id を取得するには**
  
- 呼び出し[imapisession:: queryidentity](imapisession-queryidentity.md)。 **queryidentity**は、[状態] テーブルの行の1つの**PR_RESOURCE_FLAGS**列に STATUS_PRIMARY_IDENTITY 値が存在する場合に、セッション id をベースとします。 この値が設定されている状態行がない場合、 **queryidentity**は、3つの PR_IDENTITY プロパティを設定する最初のサービスプロバイダーに id を割り当てます。 id を提供するサービスプロバイダーがない場合、 **queryidentity**は MAPI_W_NO_SERVICE を返します。 このような場合、プライマリ id として使用できる汎用ユーザーを表す文字列を作成する必要があります。 
    
 **セッションのプライマリ id を明示的に設定するには**
  
- Call [IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)。 対象のサービスプロバイダーの**MAPIUID**を渡します。 
    

