---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: ソーシャル コネクタOutlook (OSC) プロバイダーを初期化します。
ms.openlocfilehash: 4e41c78c016358c205f860345bee6cdcf3ba06e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608866"
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

