---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: ソーシャル ネットワークの一意の識別子を表す GUID を返します。
ms.openlocfilehash: 3e8e4e4f4fc2ed0a1f853e3f7dee8796ef661805
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560334"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

ソーシャル ネットワークの一意の識別子を表す GUID を返します。
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>プロパティ値

ソーシャル ネットワークの一意の識別子を表す GUID 値へのポインター。
  
## <a name="remarks"></a>注釈

GUID は変更できない必要があります。プロバイダーのバージョンが変更された場合でも変更できません。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

