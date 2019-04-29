---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434474"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスのプロバイダーテーブルへのアクセスを提供します。これには、メッセージサービスのサービスプロバイダーの一覧が含まれます。
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番プロバイダーテーブルの列に返される文字列の型を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、列は ANSI 形式になります。
    
 _lpptable_
  
> 読み上げプロバイダテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダーテーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IProviderAdmin:: getprovidertable**メソッドは、メッセージサービスのプロバイダーテーブルへのポインターを取得します。これには、メッセージサービスの各サービスプロバイダーに関する情報を含む MAPI が保持するテーブルがあります。 
  
[IMsgServiceAdmin:: getprovidertable](imsgserviceadmin-getprovidertable.md)メソッドによって返されるプロバイダーテーブルとは異なり、 **IProviderAdmin:: getprovidertable**によって返されるプロバイダテーブルには、1つまたは複数のに関連付けられている情報を表す追加の行が含まれている場合があります。メッセージサービスのサービスプロバイダー。 この追加情報は、mapisvc.inf ファイルの "Sections" キーワードを使用して、プロファイルに追加されます。 プロバイダーに特別なプロファイルセクションがある場合は、これらのセクションの**MAPIUID**構造体を**PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) プロパティに格納します。 **PR_SERVICE_EXTRA_UIDS**は、[メッセージサービスプロファイル] セクションに保存されます。 
  
削除されているか、または使用されていて、削除対象としてマークされているプロバイダーは、プロバイダテーブルには含まれません。 プロバイダーテーブルは静的であるため、メッセージサービスに対する以降の追加または削除は、テーブルには反映されません。 
  
メッセージサービスにプロバイダーがない場合、 **IProviderAdmin:: getprovidertable**は、行が0で、S_OK の戻り値を持つテーブルを返します。 
  
_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 
  
このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。 
  
プロバイダテーブルの列の完全なリストについては、「[プロバイダ table](provider-tables.md)」を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プロバイダーテーブルの行をトランスポート順で取得するには、テーブルを**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) 列で並べ替えます。 
  
その他の行を含めずに、サービスプロバイダーを表す行のみを取得するには、 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列に PT_ERROR 値を持つ行に取得することを制限します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
| MsgServiceTableDlg  <br/> |CMsgServiceTableDlg:: ondisplayitem  <br/> |mfcmapi は、 **IProviderAdmin:: getprovidertable**メソッドを使用して、新しいダイアログボックスにレンダリングするプロバイダーのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

