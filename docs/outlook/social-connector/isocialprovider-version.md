---
title: i社会 alproviderversion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: このソーシャルネットワークのプロバイダーのバージョン番号を表す文字列を返します。
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285386"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

このソーシャルネットワークのプロバイダーのバージョン番号を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>プロパティ値

プロバイダーのバージョン番号を含む文字列。
  
## <a name="remarks"></a>解説

バージョン文字列は_MajorVersion_を使用する必要があります。 _MinorVersion_形式 (たとえば、1.4730)。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

