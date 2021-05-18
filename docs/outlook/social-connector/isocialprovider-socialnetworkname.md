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
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406879"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

ソーシャル ネットワーク名を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>プロパティ値

ソーシャル ネットワーク名を含む文字列。
  
## <a name="remarks"></a>注釈

Outlookソーシャル コネクタ (OSC) プロバイダーは、ソーシャル ネットワーク名をローカライズする必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

