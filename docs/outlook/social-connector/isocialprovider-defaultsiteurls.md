---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Outlook ソーシャル コネクタ (OSC) プロバイダーのサイトの Url を指定する文字列の配列を返します。
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804342"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Outlook ソーシャル コネクタ (OSC) プロバイダーのサイトの Url を指定する文字列の配列を返します。
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>プロパティ値

OSC プロバイダーのサイトの Url を表す文字列の配列を指定する構造体へのポインター。
  
## <a name="remarks"></a>注釈

プロバイダーは、複数のサイトの Url をサポートできます。 OSC では、選択したサイトの URL のプロバイダーを通知するために[ISocialSession::SiteUrl](isocialsession-siteurl.md)プロパティを設定します。 
  
OSC では、既定のサイトの URL として、配列の最初の要素を使用します。 プロバイダーは、サイトの URL の配列に追加の要素を返すことができますが、OSC を使用しないようにします。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

