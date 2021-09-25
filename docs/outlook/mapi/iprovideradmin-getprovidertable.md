---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28025b2b60ebb563064fd3960df5a5057aea97ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561377"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスのプロバイダー テーブル 、メッセージ サービス内のサービス プロバイダーの一覧へのアクセスを提供します。
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]プロバイダー テーブルの列で返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、列は ANSI 形式になります。
    
 _lppTable_
  
> [out]プロバイダー テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダー テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IProviderAdmin::GetProviderTable** メソッドは、メッセージ サービス内の各サービス プロバイダーに関する情報を含む MAPI が保持するテーブルであるメッセージ サービスのプロバイダー テーブルへのポインターを取得します。 
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドによって返されるプロバイダー テーブルとは異なり **、IProviderAdmin::GetProviderTable** によって返されるプロバイダー テーブルには、メッセージ サービス内の 1 つ以上のサービス プロバイダーに関連付けられている情報を表す追加の行が含まれる場合があります。 この追加の情報は、Mapisvc.inf ファイルの "Sections" キーワードを使用してプロファイルに追加されます。 プロバイダーに追加のプロファイル セクションがある場合、これらのセクションの **MAPIUID** 構造は PR_SERVICE_EXTRA_UIDS ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md))**プロパティに** 格納されます。 **PR_SERVICE_EXTRA_UIDS** メッセージ サービス プロファイル セクションに保存されます。 
  
削除されたプロバイダー、または使用されているが削除のマークが付いているプロバイダーは、プロバイダー テーブルには含まれません。 プロバイダー テーブルは静的です。つまり、メッセージ サービスに対する後続の追加または削除はテーブルに反映されません。 
  
メッセージ サービスにプロバイダーがない場合 **、IProviderAdmin::GetProviderTable** は、行が 0 のテーブルを返し、S_OK値を返します。 
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 
  
このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
プロバイダー テーブル内の列の完全な一覧については、「Provider [Table」を参照してください](provider-tables.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プロバイダー テーブルの行をトランスポートの順序で取得するには、テーブルを [プロパティ] **列** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) 列PR_PROVIDER_ORDINAL並べ替えてください。 
  
サービス プロバイダーを表す行 (余分な行を含めずに) のみを取得するには、PR_RESOURCE_TYPE **(** [PidTagResourceType](pidtagresourcetype-canonical-property.md)) 列の PT_ERROR の値を持つ行に取得を制限します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI は **、IProviderAdmin::GetProviderTable** メソッドを使用して、新しいダイアログ ボックスでレンダリングするプロバイダーのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

