---
title: プロバイダーテーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328463"
---
# <a name="provider-tables"></a>プロバイダーテーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーテーブルには、サービスプロバイダーに関する情報が含まれています。 2つの異なるプロバイダーテーブルがあり、両方とも MAPI によって実装され、クライアントによって使用されます。 [IMsgServiceAdmin:: getprovidertable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出してアクセスする最初のテーブルは、現在のプロファイルのすべてのプロバイダーに関する情報を保持します。 [IProviderAdmin:: getprovidertable](iprovideradmin-getprovidertable.md)を通じてアクセスされる2番目の表は、メッセージサービスのすべてのサービスプロバイダーに関する情報を格納するテーブルを作成します。
  
これらの2つのテーブルには別の違いがあります。 **IMsgServiceAdmin:: getprovidertable**で利用できるプロバイダテーブルには、サービスプロバイダを表す行のみが含まれていますが、 **IProviderAdmin:: getprovidertable**を通じて使用可能な表には、を表す行を含めることができます。サービスプロバイダーに関連付けられている追加情報。 この追加情報は、mapisvc.inf の "Sections" キーワードを使用してプロファイルに追加されます。 プロバイダーに特別なプロファイルセクションがある場合は、これらのセクションの**MAPIUID**値を**PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) プロパティに格納します。 **PR_SERVICE_EXTRA_UIDS**は、[メッセージサービスプロファイル] セクションに保存されます。 
  
次のプロパティは、両方の種類のプロバイダーテーブルで必要な列セットを作成します。
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL**([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID**([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
プロバイダーテーブルを使用して、現在のトランスポート順序を表示したり、変更したりすることができます。 現在の順序を表示するには、 **PR_RESOURCE_TYPE**プロパティが MAPI_TRANSPORT_PROVIDER に設定されている行のみを取得する制限を作成します。 その後、 **PR_PROVIDER_ORDINAL**を並べ替えキーとして使用して、テーブルを並べ替え、 [IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドまたは[hrqueryallrows](hrqueryallrows.md)関数のいずれかを使用してすべての行を取得します。 
  
トランスポート順序を変更するには、同じ制限を適用して行を取得します。 次に、トランスポートプロバイダーの一意の識別子を表す**PR_PROVIDER_UID**プロパティから値の配列を作成します。 識別子が目的の順序になったら、 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)メソッドに渡します。 
  
プロバイダーテーブルが使用可能になると、その後の変更 (プロバイダーの追加や削除など) は反映されません。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

