---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: ソーシャル ネットワークの一意の識別子を表す GUID を返します。
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804371"
---
# <a name="isocialprovidersocialnetworkguid"></a>ISocialProvider::SocialNetworkGuid

ソーシャル ネットワークの一意の識別子を表す GUID を返します。
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a>プロパティ値

ソーシャル ネットワークの一意の識別子を表す GUID 値へのポインター。
  
## <a name="remarks"></a>注釈

GUID は不変である必要があり、プロバイダーのバージョンが変更された場合でも変更する必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

