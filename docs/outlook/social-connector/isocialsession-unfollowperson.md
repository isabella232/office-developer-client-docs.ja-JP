---
title: iの入力
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: userID パラメーターで指定された人物をソーシャルネットワーク上のフレンドとして削除します。
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336779"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

_userID_パラメーターで指定された人物をソーシャルネットワーク上のフレンドとして削除します。 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>パラメーター

_userID_
  
> 順番ユーザーのソーシャルネットワークユーザー ID を含む文字列。
    
## <a name="remarks"></a>解説

_userID_パラメーターには、ソーシャルネットワーク上のユーザーの有効なユーザー ID を指定する必要があります。 
  
Outlook Social Connector (.osc) プロバイダーが、**機能**の**** XML で [ **true** ] に設定されている場合、渡されたユーザー ID がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。 プロバイダーが [**機能**] **** の値を**false**に設定している場合、プロバイダーは OSC_E_FAIL エラーを返す必要があります。 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

