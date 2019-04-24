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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338410"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信メッセージの受信者リストに追加する受信者を作成するための、1回限りのテンプレートのテーブルを返します。
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番テーブルに含まれる文字列型 (string) の列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。
    
 _lpptable_
  
> 読み上げ1回限りのテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1回限りのテーブルが正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、アドレス帳プロバイダーが unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、アドレス帳プロバイダーが unicode のみをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーでは、1回限りのテンプレートは提供されません。
    
## <a name="remarks"></a>解説

MAPI は、 **getoneofftable**メソッドを呼び出して、受信者を作成するために1回限りのテンプレートを使用できるようにします。 新しい受信者が送信メッセージの受信者一覧に追加されます。 アドレス帳プロバイダーは、テンプレートの変更を MAPI に通知するために、1回限りのテーブルに対する通知をサポートする必要があります。 MAPI は、動的更新を有効にするために、1回限りのテーブルを開いたままにします。 
  
また、アドレス帳プロバイダーは、各コンテナーに対して1回限りのテーブルをサポートすることもできます。 発信者は、コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することによって、この1回限りのテーブルを取得します。 この表で使用できるテンプレートは、受信者をコンテナーに追加するために使用されます。 2種類の一度限りのテーブルの違いについては、「 [1 回限りのテーブルの実装](implementing-one-off-tables.md)」を参照してください。
  
アドレス帳プロバイダーの1回限りのテーブルで必要な列の一覧については、「 [1 回限りのテーブル](one-off-tables.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

