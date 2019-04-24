---
title: i指定 alprovider/networkname
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: ソーシャルネットワーク名を表す文字列を返します。
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285492"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

ソーシャルネットワーク名を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>プロパティ値

ソーシャルネットワーク名を含む文字列。
  
## <a name="remarks"></a>解説

Outlook social Connector (.osc) プロバイダーは、ソーシャルネットワーク名をローカライズする必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

