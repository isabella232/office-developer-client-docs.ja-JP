---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: ユーザーのピクチャ リソースを含むバイトの配列を取得します。
ms.openlocfilehash: 090dae46f97c2b937155d61ec65b87f2c635da5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629159"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

ユーザーのピクチャ リソースを含むバイトの配列を取得します。 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>パラメーター

_図_
  
> [out]人物のピクチャ リソースを表すバイトの配列を指定する構造体へのポインター。
    
## <a name="remarks"></a>注釈

サポートされているピクチャ リソースは、.bmp .jpeg、または .png形式です。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

