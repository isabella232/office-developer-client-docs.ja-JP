---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412913"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つの符号なし32ビット整数を別の数値で乗算します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>パラメーター

 _Multiplicand_
  
> 順番_乗数_パラメーターの値で乗算する、符号なしの32ビット整数を含む二重の単語。 
    
 _べき乗_
  
> 順番符号なし32ビットの整数乗数を含む二重の単語。
    
## <a name="return-value"></a>戻り値

**FtMulDwDw**関数は、2つの整数の積を含む[FILETIME](filetime.md)構造を返します。 2つの入力パラメーターは変更されません。 
  

