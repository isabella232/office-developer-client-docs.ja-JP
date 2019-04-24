---
title: i社会 alproviderdefaultsiteurls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Outlook Social Connector (.osc) プロバイダーのサイト url を指定する文字列の配列を返します。
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285857"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Outlook Social Connector (.osc) プロバイダーのサイト url を指定する文字列の配列を返します。
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>プロパティ値

.osc プロバイダーのサイト url を表す文字列の配列を指定する構造体へのポインター。
  
## <a name="remarks"></a>解説

プロバイダーは複数のサイト url をサポートできます。 .osc は、選択されているサイトの URL をプロバイダーに通知するために、i// [SiteUrl](isocialsession-siteurl.md)プロパティを設定します。 
  
.osc は、配列の最初の要素を既定のサイト URL として使用します。 プロバイダーは、サイト URL 配列の追加の要素を返すことができますが、.osc はそれらを使用しません。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

