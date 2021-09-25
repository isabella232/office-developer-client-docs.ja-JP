---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bc20d10e20a170a12d30053e35c79718ac088db1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567285"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル内のサービス プロバイダーの一覧であるプロバイダー テーブルへのアクセスを提供します。
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]常に NULL。
    
 _lppTable_
  
> [out]プロバイダー テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダー テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::GetProviderTable** メソッドは、プロファイルに現在インストールされているすべてのアドレス帳、メッセージ ストア、およびトランスポート プロバイダーを一覧表示する MAPI プロバイダー テーブルへのアクセスを提供します。 
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)メソッドを介して返されるプロバイダー テーブルとは異なり **、IMsgServiceAdmin::GetProviderTable** を介して返されるプロバイダー テーブルには、プロファイル内の 1 つ以上のサービス プロバイダーに関連付けられた情報を表す追加の行を含めできません。 
  
削除されたプロバイダー、または使用されているが削除のマークが付いているプロバイダーは、プロバイダー テーブルには含まれません。 プロバイダー テーブルは静的です。つまり、プロファイルへの以降の追加またはプロファイルからの削除はテーブルに反映されません。 
  
プロファイルにプロバイダーがない場合 **、GetProviderTable** は行が 0 のテーブルを返し、その値S_OK返します。 
  
プロバイダー テーブル内の列の完全な一覧については、「Provider [Table」を参照してください](provider-tables.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プロバイダー テーブルの行をトランスポート順序で取得するには、次の手順を使用します。
  
1. [IMAPITable::Restrict](imapitable-restrict.md)メソッドを呼び出して、PR_RESOURCE_TYPE **(** [PidTagResourceType](pidtagresourcetype-canonical-property.md)) プロパティと一致するプロパティ制限を適用MAPI_TRANSPORT_PROVIDER。
    
2. [IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出して、テーブルを [PR_PROVIDER_ORDINAL **]** 列 [(PidTagProviderOrdinal)](pidtagproviderordinal-canonical-property.md)列で並べ替えてください。 
    
3. [IMAPITable::QueryRows メソッドを呼](imapitable-queryrows.md)び出して、テーブルの行を取得します。 
    
これらの呼び出しの代わりに、適切なすべてのデータ構造が渡された [HrQueryAllRows](hrqueryallrows.md) 関数を 1 回呼び出す方法があります。 
  
各行で **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を取得する場合は、 **この MAPIUID** 構造体の配列を使用して [、IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)の呼び出しでトランスポート順序を設定できます。
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると、次の手順が実行されます。 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドによってプロバイダー テーブルの最初のアクティブな列に対して返されるデータの文字列型を Unicode に設定します。 プロバイダー テーブルの最初のアクティブな列は、テーブルを含むプロバイダーが [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出す前に **QueryColumns** メソッドが返す列です。 
    
- QueryRows によってプロバイダー テーブルの最初のアクティブな行に対して返されるデータの文字列型を **Unicode に設定します**。 プロバイダー テーブルの最初のアクティブな行は、テーブルを含むプロバイダーが **SetColumns** を呼び出す前に **QueryRows** が返す行です。 
    
- プロバイダー テーブルを含むクライアントが[IMAPITable::SortTable](imapitable-sorttable.md)メソッドを呼び出す前に[、IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類を制御します。 
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

