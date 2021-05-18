---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: ソーシャル コネクタ (OSC) プロバイダーのサイト URL を指定Outlook文字列の配列を返します。
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413774"
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

