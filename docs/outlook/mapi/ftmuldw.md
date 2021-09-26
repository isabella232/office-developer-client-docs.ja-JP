---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 430eff9b19f4052a77d3792ceb4f9b3412ee79ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630853"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
符号なし 64 ビット整数を符号なし 32 ビット整数で乗算します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>パラメーター

 _べき乗_
  
> [in]符号なし 32 ビット整数乗数を含む 2 つの単語。 
    
 _Multiplicand_
  
> [in] [Multiplier パラメーターの](filetime.md) 値を乗算する符号なし 64 ビット整数を含む  _FILETIME_ 構造体。 
    
## <a name="return-value"></a>戻り値

**FtMulDw 関数** は、2 つの整数の製品を含む **FILETIME** 構造体を返します。 2 つの入力パラメーターは変更されません。 
  

