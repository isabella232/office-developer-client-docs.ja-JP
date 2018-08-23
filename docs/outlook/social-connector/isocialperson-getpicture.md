---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: 個人の画像リソースを格納するバイトの配列を取得します。
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804341"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

個人の画像リソースを格納するバイトの配列を取得します。 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>パラメーター

_画像_
  
> [out]人の画像リソースを表すバイトの配列を指定する構造体へのポインター。
    
## <a name="remarks"></a>注釈

リソースは .bmp、.jpeg、または .png 形式で、画像をサポートします。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

