---
title: プロバイダー テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803707"
---
# <a name="provider-tables"></a>プロバイダー テーブル

  
  
**適用されます**: Outlook 
  
プロバイダー テーブルには、サービス プロバイダーに関する情報が含まれています。 別のプロバイダーの 2 つのテーブルは、MAPI によって実装され、クライアントによって使用される両方。 アクセス、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出すことによって、最初の表は、すべての現在のプロファイル プロバイダーに関する情報を保持します。 2 番目のテーブルでは、 [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を使用してアクセスは、すべてのメッセージ サービスのサービス プロバイダーに関する情報を格納するテーブルを作成します。
  
これら 2 つのテーブルには、他の違いがあります。 **IMsgServiceAdmin::GetProviderTable**を通じて利用可能なプロバイダーのテーブルには、サービス ・ プロバイダーを表し、 **IProviderAdmin::GetProviderTable**を使用可能なテーブルを表す行を含めることがある行だけが含まれています。サービス プロバイダーに関連付けられている追加の情報です。 MAPISVC.INF の「項目」キーワードを使用してプロファイルには、この余分な情報が追加されます。 プロバイダーに追加のプロファイル セクションが設定されているときは、 **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) のプロパティでこれらのセクションで**MAPIUID**の値を格納します。 **PR_SERVICE_EXTRA_UIDS**は、サービス プロファイルの [メッセージ] セクションに保存されます。 
  
次のプロパティは、必須の列が両方の種類のプロバイダーのテーブルで設定を構成します。
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL**([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID**([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME**([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID**([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
現在のトランスポートの順番を表示する、またはそれを変更するのには、プロバイダーのテーブルを使用できます。 現在の注文を表示するには、MAPI_TRANSPORT_PROVIDER に**PR_RESOURCE_TYPE**プロパティを使用してこれらの行だけを取得するために制限を作成します。 使用して**PR_PROVIDER_ORDINAL**の並べ替えキーとしてテーブルを並べ替えるし、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドまたは[HrQueryAllRows](hrqueryallrows.md)関数のいずれかでのすべての行を取得します。 
  
トランスポートの順番を変更するに同じ制限を適用し、行を取得します。 トランスポート プロバイダーの一意の識別子を表す、 **PR_PROVIDER_UID**プロパティからの値の配列を作成します。 識別子は、目的の順序では、ときに、 [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)メソッドに渡します。 
  
使用可能なプロバイダーのテーブルが行われて、追加またはプロバイダーの削除など、その後の変更は反映されません。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

