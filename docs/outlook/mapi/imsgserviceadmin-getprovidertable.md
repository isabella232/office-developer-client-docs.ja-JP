---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800975"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**適用対象**: Outlook 
  
プロバイダー テーブル、プロファイル内のサービス プロバイダーの一覧へのアクセスを提供します。
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]常に NULL を返します。
    
 _lppTable_
  
> [out]プロバイダー テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロバイダー テーブルは正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::GetProviderTable**メソッドでは、MAPI プロバイダーのテーブル、すべてのアドレス帳、メッセージ ・ ストア、およびプロファイルに現在インストールされているトランスポート プロバイダーの一覧が表示されるテーブルへのアクセスを提供します。 
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)メソッドによって返されるプロバイダー テーブルとは異なり、 **IMsgServiceAdmin::GetProviderTable**によって返されるプロバイダー テーブルが関連付けられている情報を表す追加の行を含めることはできません。プロファイルのサービスのプロバイダーの 1 つまたは複数の 
  
削除されている、または使用中だが、削除対象としてマークされているプロバイダーは、プロバイダーの表には含まれません。 プロバイダー テーブルへの後の追加や、プロファイルからの削除が表に反映されていないことを意味します。 
  
プロバイダー プロファイルがない場合は、 **GetProviderTable**は、0 個の行と S_OK の戻り値を持つテーブルを返します。 
  
プロバイダー テーブル内の列の一覧は、[プロバイダーのテーブル](provider-tables.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

トランスポートの順番でプロバイダーのテーブルの行を取得するには、次の手順に従います。
  
1. MAPI_TRANSPORT_PROVIDER と**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) のプロパティに一致するプロパティの制限を適用する[IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出します。
    
2. **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) の列でテーブルを並べ替えるには[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出します。 
    
3. テーブルの行を取得する[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。 
    
代わりにこれらの呼び出しは、すべての適切なデータ構造体が渡されると、 [HrQueryAllRows](hrqueryallrows.md)関数を 1 つの呼び出しを行うには。 
  
**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列にそれぞれの行を取得する場合は、 [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)への呼び出しのトランスポートの順番を設定するのには、この**MAPIUID**の構造体の配列を使用できます。
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定は、次を行います。 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドによって、プロバイダーのテーブルの最初のアクティブな列に返されるデータの unicode 文字列の種類を設定します。 プロバイダー テーブルの最初のアクティブな列は、これらの列がテーブルの呼び出しを[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドに含まれているプロバイダーの前に、 **QueryColumns**メソッドを返します。 
    
- **スプーラー**によって、プロバイダーのテーブルの最初のアクティブな行に返されるデータの unicode 文字列の種類を設定します。 プロバイダーのテーブルの最初のアクティブな行は、これらの行をテーブル呼び出し**SetColumns**を含むプロバイダーをする前に**スプーラー**を返しますです。 
    
- プロバイダー テーブルを含んでいるクライアントは、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出す前に、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類を制御します。 
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

