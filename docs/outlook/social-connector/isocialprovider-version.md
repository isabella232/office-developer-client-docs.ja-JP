---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を返します。
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804357"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を返します。 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>プロパティ値

プロバイダーのバージョン番号を含む文字列です。
  
## <a name="remarks"></a>注釈

バージョン文字列は、 _MajorVersion_を使用してください。 _マイナー バージョン_の形式 (たとえば、1.4730) です。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

