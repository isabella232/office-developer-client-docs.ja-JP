---
title: i、alproviderload
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Outlook Social Connector (.osc) プロバイダーを初期化します。
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285760"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Outlook Social Connector (.osc) プロバイダーを初期化します。
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>パラメーター

_このバージョンの形式_
  
> 順番.osc が想定する .osc プロバイダインターフェイスのバージョン。
    
_言語タグ_
  
> 順番[[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)および[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)で定義されている、現在の Outlook ユーザーインターフェイス言語を表すインターネット技術標準化委員会 (IETF) 言語タグ。
    
## <a name="remarks"></a>解説

指定されたパラメーター __ のバージョンは_X_です。_xxxx_。ここで、 _X_はメジャーバージョン、 _xxxx_は .osc のマイナーバージョンです。 Office 2013 の場合は、メジャーバージョンが15であるかどうかを確認します。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

