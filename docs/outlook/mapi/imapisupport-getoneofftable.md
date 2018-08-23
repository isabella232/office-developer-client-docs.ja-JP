---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d54487928abcc889441ec9bf89ab6a10e5290062
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570836"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI の一時テーブル (すべてのアドレスが新しい受信者を作成するためのサポートについてプロバイダーを登録しているテンプレートの一覧) へのポインターを返します。
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]文字列型の列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> Unicode 形式では、文字列型の列です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。
    
 _lppTable_
  
> [out]一時テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 一時テーブルが正常に取得しました。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::GetOneOffTable**メソッドを実装します。 アドレス帳プロバイダーは、新しい受信者を作成するためのテンプレートの完全な一覧を取得するために**GetOneOffTable**を呼び出します。 このテーブルには、MAPI をサポートしているテンプレートと同様に、セッションでアクティブになっているアドレス帳プロバイダーがサポートするテンプレートが含まれています。 
  
新しく作成された受信者は、メッセージの宛先を使用することができますか、アドレス帳コンテナーに追加することができます。
  
必須の列を一時テーブルの設定を構成するプロパティのリストは、[一時テーブル](one-off-tables.md)を参照してください。
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

この一時テーブルへの変更の通知を受信する登録している場合は、他のプロバイダーの一時テーブルへの変更の通知も表示されます。 これらの通知に基づき、現在のセッション中に追加される新しいアドレスの種類をサポートできます。
  
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[PidTagCreateTemplates 標準プロパティ Property](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[1 回限りのテーブル](one-off-tables.md)

