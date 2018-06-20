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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801167"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**適用されます**: Outlook 
  
メッセージ サービスのプロバイダーのテーブル、メッセージ サービスのサービス プロバイダーの一覧へのアクセスを提供します。
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]プロバイダー テーブルの列で返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> Unicode 形式では、文字列型の列です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の列です。
    
 _lppTable_
  
> [out]プロバイダー テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロバイダー テーブルは正常に返されました。
    
## <a name="remarks"></a>備考

**IProviderAdmin::GetProviderTable**メソッドは、メッセージ サービスのプロバイダーのテーブル、MAPI は、メッセージ サービスでは、各サービス プロバイダーに関する情報が含まれていることを保持するテーブルへのポインターを取得します。 
  
、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドによって返されるプロバイダーのテーブルとは異なり、 **IProviderAdmin::GetProviderTable**によって返されるプロバイダーのテーブルがのいずれかに関連付けられている情報を表す追加の行を含めることがメッセージ サービスのサービス プロバイダーです。 この追加情報は、Mapisvc.inf ファイルの「項目」キーワードを使用してプロファイルに追加されます。 プロバイダーに追加のプロファイル セクションが設定されているときは、 **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) のプロパティでこれらのセクションの**MAPIUID**構造体を格納します。 **PR_SERVICE_EXTRA_UIDS**は、サービス プロファイルの [メッセージ] セクションに保存されます。 
  
削除されている、または使用中だが、削除対象としてマークされているプロバイダーは、プロバイダーの表には含まれません。 プロバイダー テーブルにそれ以降に追加された機能またはメッセージ サービスからの削除が表に反映されていないことを意味します。 
  
メッセージ サービスには、プロバイダーがなければ、 **IProviderAdmin::GetProviderTable**は、0 個の行と S_OK の戻り値を持つテーブルを返します。 
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 
  
このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
プロバイダー テーブル内の列の一覧は、[プロバイダーのテーブル](provider-tables.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

トランスポートの順番でプロバイダーのテーブルの行を取得するには、 **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) の列でテーブルをソートします。 
  
(せず、余分な行を含む) のサービス ・ プロバイダーを表す行のみを取得するには、PT_ERROR の**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))] 列の値を持つ行が取得されるを制限します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI では、 **IProviderAdmin::GetProviderTable**メソッドを使用して、新しいダイアログ ボックスに表示するプロバイダーのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin: IUnknown](iprovideradminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

