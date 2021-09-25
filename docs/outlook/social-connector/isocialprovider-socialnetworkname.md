---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: ソーシャル ネットワーク名を表す文字列を返します。
ms.openlocfilehash: 400765e72567bb5e24bf806c279a02619ccefaa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574518"
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

