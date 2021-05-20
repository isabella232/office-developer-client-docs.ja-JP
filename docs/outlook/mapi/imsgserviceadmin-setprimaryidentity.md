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
  
メッセージ サービスをプロファイルのプライマリ ID のサプライヤーに指定します。
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]**SetPrimaryIdentity** が現在の ID をクリアする必要があるという、プライマリ ID (NULL) を指定するメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ サービスは、プライマリ ID のサプライヤーに正常に割り当てされました。
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity は**、PR_RESOURCE_FLAGS ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに SERVICE_NO_PRIMARY_IDENTITY フラグ **が設定** されているメッセージ サービスを指定しようとした。
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::SetPrimaryIdentity** メソッドは、プロファイルのプライマリ ID のサプライヤーとしてメッセージ サービスを確立します。 プライマリ ID は、通常、メッセージ サービスにログオンしているユーザーです。 これは、次の 3 つのプロパティで表されます。 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
指定されたメッセージ サービスのすべてのサービス プロバイダーは、これら 3 つのプロパティを、プライマリ ID を提供するメッセージング ユーザーの表示名、エントリ識別子、および検索キーに設定します。 クライアントは [、IMAPISession::QueryIdentity](imapisession-queryidentity.md) メソッドを呼び出すことによって、プライマリ ID のエントリ識別子を取得できます。 
  
**PR_RESOURCE_FLAGS** プロパティは、プライマリ ID を提供するメッセージ サービスのメンバーであるプロバイダー、およびメッセージ サービスの SERVICE_PRIMARY_IDENTITY に対して STATUS_PRIMARY_IDENTITY に設定されます。 サービス プロバイダーがメッセージ サービスのプライマリ ID を指定できない場合、サービス プロバイダーはメッセージ サービス **PR_RESOURCE_FLAGSに** STATUS_NO_PRIMARY_IDENTITY。 **SetPrimaryIdentity** は、PR_RESOURCE_FLAGS **ID** を指定していない各メッセージ サービスの SERVICE_NO_PRIMARY_IDENTITY プロパティを設定します。 
  
MAPI に関する情報を持つ各メッセージ サービス プロバイダーは、クライアントがサービスにログオンするときに、各ユーザーの ID を確立できます。 ただし、MAPI は MAPI セッションごとに複数のサービス プロバイダーへの接続をサポートするため、MAPI セッション全体に対して特定のユーザーの ID をしっかりと定義する必要はありません。ユーザーの ID は、どのサービスが関係するかによって異なります。 クライアントは **SetPrimaryIdentity** を呼び出して、メッセージ サービスによってユーザーに対して確立された多数の ID の 1 つをそのユーザーのプライマリ ID として指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

