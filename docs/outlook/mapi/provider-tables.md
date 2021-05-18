---
title: プロバイダー テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408972"
---
# <a name="provider-tables"></a>プロバイダー テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダー テーブルには、サービス プロバイダーに関する情報が含まれる。 MAPI によって実装され、クライアントによって使用される 2 つの異なるプロバイダー テーブルがあります。 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出すことによってアクセスされる最初のテーブルには、現在のプロファイルのすべてのプロバイダーに関する情報が保持されます。 [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を介してアクセスされる 2 番目のテーブルは、メッセージ サービスのすべてのサービス プロバイダーに関する情報を格納するテーブルを作成します。
  
これら 2 つのテーブルには別の違いがあります。 **IMsgServiceAdmin::GetProviderTable** で使用できるプロバイダー テーブルには、サービス プロバイダーを表す行だけが含まれますが **、IProviderAdmin::GetProviderTable** を使用して使用できるテーブルには、サービス プロバイダーに関連付けられた追加情報を表す行が含まれる場合があります。 この追加の情報は、MAPISVC.INF の "Sections" キーワードを使用してプロファイルに追加されます。 プロバイダーに追加のプロファイル セクションがある場合、これらのセクションの **MAPIUID** 値は PR_SERVICE_EXTRA_UIDS ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md))**プロパティに** 格納されます。 **PR_SERVICE_EXTRA_UIDS** メッセージ サービス プロファイル セクションに保存されます。 
  
次のプロパティは、両方の種類のプロバイダー テーブルで必要な列セットを構成します。
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
プロバイダー テーブルは、現在のトランスポートの順序を表示したり、変更したりするために使用できます。 現在の順序を表示するには、PR_RESOURCE_TYPE プロパティが設定されている行のみを取得MAPI_TRANSPORT_PROVIDER。 次に **PR_PROVIDER_ORDINAL** を並べ替えキーとして使用し [、IMAPITable::QueryRows](imapitable-queryrows.md) メソッドまたは [HrQueryAllRows](hrqueryallrows.md) 関数を使用してすべての行を取得します。 
  
トランスポートの順序を変更するには、同じ制限を適用して行を取得します。 次に、トランスポート プロバイダーの一意の識別子 **PR_PROVIDER_UID** プロパティから値の配列を作成します。 識別子が目的の順序である場合は、 [それらを IMsgServiceAdmin::MsgServiceTransportOrder メソッドに渡](imsgserviceadmin-msgservicetransportorder.md) します。 
  
プロバイダー テーブルが使用可能にされた後、プロバイダーの追加や削除など、後続の変更は反映されません。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

