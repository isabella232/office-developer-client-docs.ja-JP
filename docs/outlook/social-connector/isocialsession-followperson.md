---
title: i社会 alsessionん
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: ソーシャルネットワークにログオンしているユーザーのフレンドとして、emailAddress パラメーターによって識別された人物を追加します。
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285365"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

ソーシャルネットワークにログオンしているユーザーのフレンドとして、 _emailAddress_パラメーターによって識別された人物を追加します。 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>パラメーター

_emailAddress_
  
> 順番個人の電子メールアドレスを含む文字列。
    
## <a name="remarks"></a>解説

_emailAddress_パラメーターは、有効な SMTP アドレスであることが必要です。 Outlook Social Connector (.osc) プロバイダーが、**機能**では**** 、 _emailAddress_の引数が**true**として設定されており、その引数がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND を返す必要があります。エラー. プロバイダーが**権限**で OSC_E_FAIL **** を**false**として設定している場合、プロバイダーはエラーを返す必要があります。
  
プロバイダーが[ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装していて**** 、**機能**に**true**として ISocialSession2 が設定されている場合、.osc は、i alsession:::/の代わりに、 [::](isocialsession2-followpersonex.md)のようにします。 ****. プロバイダーが**ISocialSession2**インターフェイスを実装していない場合、または**ISocialSession2::** を返します。 OSC_E_NOTIMPL エラーを返します。この場合、.osc は、プロバイダーが設定**** **されている限り、i alsession:: という名前を呼び出します。****機能**につい**** ての概要 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
**isocalsession::** **ISocialSession2::** を実装するかどうかを決定するには、プロバイダーが**ISocialSession2**内の他のメソッドを必要とするかどうか、およびその方法を使用_できるかどうかを検討する必要があります。djsplayName_パラメーターを**** 指定します。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

