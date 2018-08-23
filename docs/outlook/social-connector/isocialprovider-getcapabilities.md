---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: プロバイダーの機能を説明する文字列を取得します。
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804352"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

プロバイダーの機能を説明する文字列を取得します。
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>パラメーター

_result_
  
> [out]Outlook ソーシャル コネクタ (OSC) プロバイダーの機能を表す XML 文字列です。
    
## <a name="remarks"></a>注釈

返される_結果_の XML 文字列は、OSC プロバイダーの拡張機能の XML スキーマで定義されている**機能**要素のスキーマ定義に従う必要があります。 
  
プロバイダーでは、以降、OSC からプロバイダーに正常に動作するを有効にするのには_結果_の文字列を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

