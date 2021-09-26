---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c119c9f11ad38f2cb3eaa8916e16496187dda02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610742"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージの受信者リストに追加する受信者を作成するための一時テンプレートのテーブルを返します。
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]テーブルに含まれる文字列列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。
    
 _lppTable_
  
> [out]1 回表へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1 回のテーブルが正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> アドレス帳MAPI_UNICODEフラグが設定され、アドレス帳プロバイダーが Unicode をサポートしていないか、MAPI_UNICODE が設定されていないと、アドレス帳プロバイダーは Unicode のみをサポートします。
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、1 回きりテンプレートを提供しない。
    
## <a name="remarks"></a>注釈

MAPI は **GetOneOffTable メソッドを呼** び出して、受信者を作成するために使用可能な 1 回のテンプレートを作成します。 新しい受信者は、送信メッセージの受信者リストに追加されます。 アドレス帳プロバイダーは、テンプレートの変更を MAPI に通知するために、1 回きりテーブルの通知をサポートする必要があります。 MAPI は、動的更新を有効にするための 1 回きりテーブルを開いた保持します。 
  
アドレス帳プロバイダーは、各コンテナーに対して 1 回のテーブルをサポートできます。 呼び出し元は、コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出し **、PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することで、この一時テーブルを取得します。 この表で使用できるテンプレートは、コンテナーに受信者を追加するために使用されます。 2 種類の 1 回使用テーブルの違いについては、「テーブルの実装」 [をOne-Offしてください](implementing-one-off-tables.md)。
  
アドレス帳プロバイダーの 1 回のテーブルで必要な列の一覧については [、「One-Off Tables」を参照してください](one-off-tables.md)。
  
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

