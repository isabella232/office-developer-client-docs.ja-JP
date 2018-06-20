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
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804354"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Outlook ソーシャル コネクタ (OSC) プロバイダーを初期化します。
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameters

_socialProviderInterfaceVersion_
  
> [in]OSC で予期される OSC プロバイダーのインターフェイスのバージョンです。
    
_languageTag_
  
> [in][[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt)、現在の Outlook ユーザー インターフェイスの言語を表すによって定義されているインターネット技術標準化委員会 (IETF) の言語タグ。
    
## <a name="remarks"></a>備考

_SocialProviderInterfaceVersion_パラメーターのバージョンの形式は、 _X_です。_xxxx_、 _X_はメジャー バージョンで_xxxx_は、OSC のマイナー バージョンです。 Office 2013 では、15 の中のメジャー バージョンを確認してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

