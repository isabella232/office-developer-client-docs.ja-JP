---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: ソーシャル ネットワークにログオン中のユーザーのフレンドとして、emailAddress パラメーターで識別されるユーザーを追加します。
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804364"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddress_パラメーターで識別されるユーザーを追加します。 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>パラメーター

_emailAddress_
  
> [in]人物の電子メール アドレスを含む文字列です。
    
## <a name="remarks"></a>注釈

_EmailAddress_パラメーターは、有効な SMTP アドレスである必要があります。 プロバイダーは、OSC_E_NOT_FOUND を返す必要があります、Outlook ソーシャル コネクタ (OSC) プロバイダーが設定して、 **followPerson**メソッド**は true**として**機能**、 _emailAddress_の引数は、ネットワーク上のユーザーと一致しない場合は、エラーです。 設定した場合、プロバイダー **followPerson** **false**として**の機能**で、プロバイダーは、OSC_E_FAIL エラーを返す必要があります。
  
OSC が**ISocialSession::FollowPerson の代わりに[ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出す場合は、プロバイダーでは、 [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装して、**機能**で**は** **followPerson**に設定が、**. プロバイダーに**が設定されている限りに、OSC が**ISocialSession::FollowPerson**を呼び出す場合、プロバイダー インターフェイスを実装しません、 **ISocialSession2** 、または**ISocialSession2::FollowPersonEx**には、OSC_E_NOTIMPL エラーが返されます、followPerson**として**真**に**機能**します。 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
かどうか**ISocalSession::FollowPerson**または**ISocialSession2::FollowPersonEx**を実装するにする必要があるかどうかと**ISocialSession2**、内の他のメソッドが、プロバイダーに必要があるかどうかを決定する際に、_を使用することができます。djsplayName_ **FollowPersonEx**内のパラメーターです。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

