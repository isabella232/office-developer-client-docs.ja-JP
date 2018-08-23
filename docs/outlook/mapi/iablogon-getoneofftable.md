---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3732d8cbfaf9a6a10c62eae9e7a12b04de8a80ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583681"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
送信メッセージの受信者の一覧に追加する受信者を作成するための 1 回限りのテンプレートのテーブルを返します。
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]テーブルに含まれている文字列型の列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> Unicode 形式では、文字列型の列です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。
    
 _lppTable_
  
> [out]一時テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 一時テーブルが正常に取得しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されたアドレス帳プロバイダーが Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、アドレス帳プロバイダーは、Unicode だけをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、1 回限りのテンプレートを提供していません。
    
## <a name="remarks"></a>注釈

MAPI では、受信者を作成するのには使用可能な 1 回限りのテンプレートを作成する**GetOneOffTable**メソッドを呼び出します。 新しい受信者は、送信メッセージの受信者の一覧に追加されます。 アドレス帳プロバイダーは、MAPI のテンプレートの変更を通知するために一時テーブルの通知をサポートする必要があります。 MAPI では、動的更新を有効にするのには開いている一時テーブルを保持します。 
  
アドレス帳プロバイダーは、そのコンテナーの一時テーブルをサポートできます。 呼び出し元は、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すと、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを要求して、この一時テーブルを取得します。 このテーブルを使用できるテンプレートを使用すると、コンテナーに受信者を追加します。 一時テーブルの 2 つの種類の違いについては、[一時テーブルを実装する](implementing-one-off-tables.md)を参照してください。
  
アドレス帳プロバイダーの一時テーブルに必要な列のリストは、[一時テーブル](one-off-tables.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

