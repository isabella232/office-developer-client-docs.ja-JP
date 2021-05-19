---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: ソーシャル ネットワーク上のフレンドとして userID パラメーターによって識別されたユーザーを削除します。
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418436"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

ソーシャル ネットワーク上のフレンドとして  _userID_ パラメーターによって識別されたユーザーを削除します。 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>パラメーター

_userID_
  
> [in]ユーザーのソーシャル ネットワーク ユーザー ID を含む文字列。
    
## <a name="remarks"></a>注釈

_userID パラメーター_ は、ソーシャル ネットワーク上のユーザーの有効なユーザー ID である必要があります。 
  
Outlook Social Connector (OSC) プロバイダーが機能の XML で **doNotFollowPerson** を true に設定している場合、渡されたユーザー ID がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。  プロバイダーが **doNotFollowPerson** を機能で **false** に設定している場合、プロバイダーはエラーメッセージをOSC_E_FAILします。 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

