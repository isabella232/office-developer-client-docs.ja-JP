---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Outlook ソーシャル コネクタ (OSC) プロバイダーを初期化します。
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385831"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Outlook ソーシャル コネクタ (OSC) プロバイダーを初期化します。
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>パラメーター

_socialProviderInterfaceVersion_
  
> [in]OSC で予期される OSC プロバイダーのインターフェイスのバージョンです。
    
_languageTag_
  
> [in][[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)、現在の Outlook ユーザー インターフェイスの言語を表すによって定義されているインターネット技術標準化委員会 (IETF) の言語タグ。
    
## <a name="remarks"></a>備考

_SocialProviderInterfaceVersion_パラメーターのバージョンの形式は、 _X_です。_xxxx_、 _X_はメジャー バージョンで_xxxx_は、OSC のマイナー バージョンです。 Office 2013 では、15 の中のメジャー バージョンを確認してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

