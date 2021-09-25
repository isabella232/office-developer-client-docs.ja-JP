---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: プロバイダーの機能を説明する文字列を取得します。
ms.openlocfilehash: d0c6772d38d0bdf6d1c6d3b482eb0dc7b70f7f50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574511"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

プロバイダーの機能を説明する文字列を取得します。
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>パラメーター

_result_
  
> [out]ソーシャル コネクタ (OSC) プロバイダーの機能Outlook XML 文字列。
    
## <a name="remarks"></a>注釈

返  _される結果_ XML 文字列は、OSC プロバイダーの機能拡張のための XML スキーマで定義されている **、capabilities** 要素のスキーマ定義に準拠している必要があります。 
  
プロバイダーは、OSC  _からプロバイダー_ への後続の呼び出しが正しく動作するように、結果文字列を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

