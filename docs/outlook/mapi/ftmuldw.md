---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328001"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
符号なしの64ビット整数を、符号なしの32ビット整数で乗算します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>パラメーター

 _べき乗_
  
> 順番符号なし32ビットの整数乗数を含む二重の単語。 
    
 _Multiplicand_
  
> 順番_乗数_パラメーターの値で乗算する、符号なしの64ビット整数を含む[FILETIME](filetime.md)構造。 
    
## <a name="return-value"></a>戻り値

**FtMulDw**関数は、2つの整数の積を含む**FILETIME**構造を返します。 2つの入力パラメーターは変更されません。 
  

