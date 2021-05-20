---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438275"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>プロパティ値

プロバイダーのバージョン番号を含む文字列。
  
## <a name="remarks"></a>注釈

バージョン文字列は  _MajorVersion を使用する必要があります_。 _MinorVersion_ 形式 (1.4730 など)。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

