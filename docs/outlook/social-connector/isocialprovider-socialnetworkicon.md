---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: ソーシャル ネットワークのアイコンを表すバイトの配列を返します。
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804482"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

ソーシャル ネットワークのアイコンを表すバイトの配列を返します。 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>プロパティ値

ソーシャル ネットワークのアイコンが含まれているバイトの配列を指定する構造体へのポインター。
  
## <a name="remarks"></a>注釈

画像がサポートされているリソースとは、.bmp、.jpeg、および .png 形式です。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

