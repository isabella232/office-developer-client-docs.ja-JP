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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800992"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**適用されます**: Outlook 
  
メッセージ サービス プロファイルのプライマリ id のサプライヤーになることを指定します。
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in]主の id を指定するのにはメッセージ サービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体または**SetPrimaryIdentity**が現在の id をクリアする必要があることを示す、NULL へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービスは、プライマリ id の提供元を正常に割り当てられました。
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity**では、SERVICE_NO_PRIMARY_IDENTITY フラグの**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティを設定するメッセージ サービスを指定しようとしています。
    
## <a name="remarks"></a>備考

**IMsgServiceAdmin::SetPrimaryIdentity**メソッドは、プロファイルのプライマリ id の提供元として、メッセージ サービスを確立します。 プライマリ id は、通常はメッセージ サービスにログオンしているユーザーです。 3 つのプロパティによって表されます。 
  
- **PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
指定されたメッセージ サービスですべてのサービス プロバイダーは、表示名、エントリ id、およびプライマリ id を提供するメッセージングのユーザーのキーを検索するにはこれら 3 つのプロパティを設定します。 クライアントは、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)メソッドを呼び出すことによって、プライマリ id のエントリ id を取得できます。 
  
主の id を提供するメッセージ サービスのメンバーであるすべてのプロバイダーの STATUS_PRIMARY_IDENTITY とメッセージ サービスの SERVICE_PRIMARY_IDENTITY、 **PR_RESOURCE_FLAGS**プロパティが設定されています。 サービス プロバイダーは、メッセージ サービスのプライマリ id を提供できません、 **PR_RESOURCE_FLAGS**を STATUS_NO_PRIMARY_IDENTITY に設定します。 **SetPrimaryIdentity**は、SERVICE_NO_PRIMARY_IDENTITY をプライマリ id を指定していないが、各メッセージ サービスの**PR_RESOURCE_FLAGS**プロパティを設定します。 
  
クライアントがサービスにログオンすると、MAPI には詳細情報が含まれているメッセージの各サービス プロバイダーは、ユーザーごとの id を確立できます。 ただし、MAPI は MAPI セッションごとに複数のサービス プロバイダーへの接続をサポートするためは全体として、MAPI セッションの特定のユーザーの id の定義をしっかりユーザーの id は、どのサービスが含まれているによって異なります。 クライアントは、そのユーザーのプライマリ id として、ユーザーのメッセージ サービスによって確立された多くのユーザーのいずれかを指定するのには**SetPrimaryIdentity**を呼び出すことができます。 
  
## <a name="see-also"></a>関連項目



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)

