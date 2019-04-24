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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317382"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーテーブルへのアクセスを提供します。これは、プロファイル内のサービスプロバイダーの一覧です。
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番常に NULL。
    
 _lpptable_
  
> 読み上げプロバイダテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダーテーブルが正常に返されました。
    
## <a name="remarks"></a>解説

**IMsgServiceAdmin:: getprovidertable**メソッドは、プロファイルに現在インストールされているすべてのアドレス帳、メッセージストア、およびトランスポートプロバイダーを一覧表示した MAPI プロバイダーテーブルへのアクセスを提供します。 
  
[IProviderAdmin:: getprovidertable](iprovideradmin-getprovidertable.md)メソッドによって返されるプロバイダテーブルとは異なり、 **IMsgServiceAdmin:: getprovidertable**を通じて返されるプロバイダテーブルには、関連付けられている情報を表す追加の行を含めることができませんプロファイルに1つ以上のサービスプロバイダーがある。 
  
削除されているか、または使用されていて、削除対象としてマークされているプロバイダーは、プロバイダテーブルには含まれません。 プロバイダーテーブルは静的であるため、プロファイルからの以降の追加または削除がテーブルに反映されることはありません。 
  
プロファイルにプロバイダーが含まれていない場合、 **getprovidertable**は0行と S_OK 戻り値を持つテーブルを返します。 
  
プロバイダテーブルの列の完全なリストについては、「[プロバイダ table](provider-tables.md)」を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プロバイダーテーブルの行をトランスポート順で取得するには、次の手順を使用します。
  
1. **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) プロパティに一致するプロパティ制限を MAPI_TRANSPORT_PROVIDER に適用するには、 [IMAPITable:: Restrict](imapitable-restrict.md)メソッドを呼び出します。
    
2. **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) 列でテーブルを並べ替えるには、 [IMAPITable:: sorttable](imapitable-sorttable.md)メソッドを呼び出します。 
    
3. [IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出して、テーブルの行を取得します。 
    
これらの呼び出しに代わる方法として、すべての適切なデータ構造を渡すことで、 [hrqueryallrows](hrqueryallrows.md)関数への1回の呼び出しを行う方法があります。 
  
各行の**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を取得する場合は、この**MAPIUID**構造体の配列を使用して、 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)の呼び出しでトランスポートの順序を設定できます。
  
_ulflags_パラメーターに MAPI_UNICODE フラグを設定すると、次の処理が行われます。 
  
- 文字列の種類を Unicode に設定し、 [IMAPITable:: querycolumns](imapitable-querycolumns.md)メソッドによってプロバイダテーブルの最初のアクティブな列に対して返されるデータを指定します。 プロバイダーテーブルの最初のアクティブな列は、テーブルを含むプロバイダーが[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出す前に**querycolumns**メソッドが返す列です。 
    
- **QueryRows**によってプロバイダテーブルの最初のアクティブな行に対して返されるデータについて、文字列の種類を Unicode に設定します。 プロバイダーテーブルの最初のアクティブな行は、そのテーブルを含むプロバイダーが**SetColumns**を呼び出す前に**QueryRows**が返す行です。 
    
- は、プロバイダーテーブルを含むクライアントが[imapitable:: sorttable](imapitable-sorttable.md)メソッドを呼び出す前に、 [imapitable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類を制御します。 
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

