---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: ソーシャル コネクタOutlook (OSC) プロバイダーを初期化します。
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285760"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

ソーシャル コネクタOutlook (OSC) プロバイダーを初期化します。
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>パラメーター

_socialProviderInterfaceVersion_
  
> [in]OSC で予期される OSC プロバイダー インターフェイスのバージョン。
    
_languageTag_
  
> [in][[RFC4646] および [RFC4647]](https://www.ietf.org/rfc/rfc4646.txt)で定義されるインターネット[](https://www.ietf.org/rfc/rfc4647.txt)エンジニアリング タスク フォース (IETF) 言語タグは、現在の Outlook ユーザー インターフェイス言語を表します。
    
## <a name="remarks"></a>注釈

_socialProviderInterfaceVersion_ パラメーターのバージョン形式は _X です_。_xxxx_ _、X_ はメジャー バージョン _、xxxx_ は OSC のマイナー バージョンです。 2013 Office、メジャー バージョンが 15 か確認してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

