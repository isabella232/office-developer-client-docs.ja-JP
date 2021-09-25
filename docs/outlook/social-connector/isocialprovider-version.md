---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。
ms.openlocfilehash: 5f3e285d4a22f667eaef6008982057673dfcbcd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629124"
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

