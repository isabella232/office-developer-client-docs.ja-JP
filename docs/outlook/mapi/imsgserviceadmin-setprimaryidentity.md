---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430365"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスがプロファイルのプライマリ id のサプライヤーであることを指定します。
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> 順番プライマリ id を指定するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。または NULL。これは、 **setprimaryidentity**が現在の id をクリアする必要があることを示します。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービスに、プライマリ id のサプライヤーが正常に割り当てられました。
    
MAPI_E_NO_ACCESS 
  
> **setprimaryidentity**は、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに SERVICE_NO_PRIMARY_IDENTITY フラグが設定されたメッセージサービスを指定しようとしました。
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin:: setprimaryidentity**メソッドは、プロファイルのプライマリ id のサプライヤーとしてメッセージサービスを確立します。 プライマリ id は、通常、メッセージサービスにログオンしているユーザーです。 次の3つのプロパティで表されます。 
  
- **PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
指定したメッセージサービスのすべてのサービスプロバイダーは、これら3つのプロパティを、プライマリ id を提供するメッセージングユーザーの表示名、エントリ識別子、および検索キーに設定します。 クライアントは、 [imapisession:: queryidentity](imapisession-queryidentity.md)メソッドを呼び出すことによって、プライマリ id のエントリ id を取得できます。 
  
**PR_RESOURCE_FLAGS**プロパティは、プライマリ id を提供するメッセージサービスのメンバーであるすべてのプロバイダーの STATUS_PRIMARY_IDENTITY、およびメッセージサービスの SERVICE_PRIMARY_IDENTITY に設定されます。 サービスプロバイダーがメッセージサービスのプライマリ id を提供できない場合、 **PR_RESOURCE_FLAGS**は STATUS_NO_PRIMARY_IDENTITY に設定されます。 **setprimaryidentity**は、プライマリ id を指定していない各メッセージサービスの**PR_RESOURCE_FLAGS**プロパティを SERVICE_NO_PRIMARY_IDENTITY に設定します。 
  
MAPI が情報を持っている各メッセージサービスプロバイダーは、クライアントがサービスにログオンしたときに、各ユーザーの id を確立できます。 ただし、mapi は各 mapi セッションに対して複数のサービスプロバイダーへの接続をサポートしているため、mapi セッション全体で特定のユーザーの id を定義することはありません。ユーザーの id は、関係するサービスによって異なります。 クライアントは**setprimaryidentity**を呼び出して、そのユーザーのプライマリ id として、メッセージサービスによってユーザーに対して確立された複数の id の1つを指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

