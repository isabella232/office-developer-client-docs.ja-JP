---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: ソーシャル ネットワークの友人として、ユーザー Id のパラメーターで識別されるユーザーを削除します。
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804373"
---
# <a name="isocialsessionunfollowperson"></a>ISocialSession::UnFollowPerson

ソーシャル ネットワークの友人として、_ユーザー Id_のパラメーターで識別されるユーザーを削除します。 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a>パラメーター

_ユーザー Id_
  
> [in]人のソーシャル ネットワークのユーザー ID を含む文字列です。
    
## <a name="remarks"></a>注釈

_ユーザー Id_パラメーターは、ソーシャル ネットワーク上のユーザーの有効なユーザー ID である必要があります。 
  
Outlook ソーシャル コネクタ (OSC) プロバイダーは、**該当****機能**の XML で**doNotFollowPerson**を設定するには、プロバイダーは、ユーザーの ID が渡されますが、ネットワーク上のユーザーと一致しないことの場合は OSC_E_NOT_FOUND エラーを返す必要があります。 設定した場合、プロバイダー **doNotFollowPerson** **false**として**の機能**で、プロバイダーは、OSC_E_FAIL エラーを返す必要があります。 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

