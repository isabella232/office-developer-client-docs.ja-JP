---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: ソーシャル コネクタ (OSC) プロバイダーのサイト URL を指定Outlook文字列の配列を返します。
ms.openlocfilehash: bbdd30265c45ea140361149ecc97f5678beb54b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629145"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

ソーシャル コネクタ (OSC) プロバイダーのサイト URL を指定Outlook文字列の配列を返します。
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>プロパティ値

OSC プロバイダーのサイト URL を表す文字列の配列を指定する構造体へのポインター。
  
## <a name="remarks"></a>注釈

プロバイダーは、複数のサイト URL をサポートできます。 OSC は [、ISocialSession::SiteUrl](isocialsession-siteurl.md) プロパティを設定して、選択したサイト URL をプロバイダーに通知します。 
  
OSC は、配列の最初の要素を既定のサイト URL として使用します。 プロバイダーは、サイト URL 配列内の追加の要素を返できますが、OSC はそれらを使用しません。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

