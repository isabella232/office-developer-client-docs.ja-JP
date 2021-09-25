---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: emailAddress パラメーターで識別されたユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。
ms.openlocfilehash: 6c0c4d31dd1627a13b15b0b779c2e798ab9fd64b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590409"
---
# <a name="isocialsessionfollowperson"></a>ISocialSession::FollowPerson

_emailAddress_ パラメーターで識別されたユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a>パラメーター

_emailAddress_
  
> [in]ユーザーの電子メール アドレスを含む文字列。
    
## <a name="remarks"></a>注釈

_emailAddress パラメーター_ は、有効な SMTP アドレスである必要があります。 Outlook Social Connector (OSC) プロバイダーが **followPerson** メソッドを機能でtrue に設定し _、emailAddress_ の引数がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。 プロバイダーが **followPerson** を機能で **false** に設定している場合、プロバイダーはエラー メッセージをOSC_E_FAILします。
  
プロバイダーが [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装し **、followPerson** を機能に **true** に設定している場合、OSC は **ISocialSession::FollowPerson ではなく ISocialSession2::FollowPersonEx** を呼び出します。 [](isocialsession2-followpersonex.md) プロバイダーが **ISocialSession2** インターフェイスを実装しない場合、または **ISocialSession2::FollowPersonEx** が OSC_E_NOTIMPL エラーを返す場合、プロバイダーが **followPerson** を機能で true に設定している限り、OSC は **ISocialSession::FollowPerson** を呼び出します。 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
**ISocalSession:::FollowPerson** または **ISocialSession2::FollowPersonEx** を実装するかどうかを決定する際には、プロバイダーが **ISocialSession2** で他のメソッドを必要とするかどうか、**および FollowPersonEx** で _djsplayName_ パラメーターを使用できるかどうかを検討する必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

