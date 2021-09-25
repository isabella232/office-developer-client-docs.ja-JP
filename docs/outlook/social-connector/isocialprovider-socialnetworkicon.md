---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: ソーシャル ネットワークのアイコンを表すバイトの配列を返します。
ms.openlocfilehash: f5c2b2744364f159545d72e8a2525562acc90d06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594924"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

ソーシャル ネットワークのアイコンを表すバイトの配列を返します。 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>プロパティ値

ソーシャル ネットワークのアイコンを含むバイトの配列を指定する構造体へのポインター。
  
## <a name="remarks"></a>注釈

サポートされているピクチャ リソースは、.bmp.jpeg、および .png形式です。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

