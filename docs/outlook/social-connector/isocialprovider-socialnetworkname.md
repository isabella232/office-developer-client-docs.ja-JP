---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: ソーシャル ネットワーク名を表す文字列を返します。
ms.openlocfilehash: 78424db0940b2c23914355b2b20ba5bc531ad3ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804356"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

ソーシャル ネットワーク名を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>プロパティ値

ソーシャル ネットワーク名を含む文字列です。
  
## <a name="remarks"></a>備考

Outlook ソーシャル コネクタ (OSC) プロバイダーには、ソーシャル ネットワークの名前をローカライズする必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

