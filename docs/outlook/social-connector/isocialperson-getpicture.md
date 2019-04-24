---
title: i形式 al個人 getpicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: ユーザーの picture リソースを含むバイトの配列を取得します。
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331655"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

ユーザーの picture リソースを含むバイトの配列を取得します。 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>パラメーター

_表_
  
> 読み上げ個人の画像リソースを表すバイト配列を指定する構造体へのポインター。
    
## <a name="remarks"></a>解説

サポートされている画像リソースは .bmp、.jpeg、または .png 形式です。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

