---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429706"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
符号なしの64ビット整数をもう1つ別に追加します。オプションで、キャリーフラグを使用します。
  
|||
|:-----|:-----|
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>パラメーター

 _ft1_
  
> 順番追加する最初の未署名の64ビット整数を含む[FILETIME](filetime.md)構造体。 
    
 _ft2_
  
> 順番追加する2番目の符号なし64ビット整数を含む FILETIME 構造。
    
 _pwCarry_
  
> [入力、出力、オプション]入力時に、着信キャリーフラグへのポインター。 出力時に、追加のキャリー結果へのポインター。 キャリー result が必要ない場合は、このパラメーターを NULL にすることができます。
    
## <a name="return-value"></a>戻り値

**ftadcft**関数は、2つの整数の合計を含む**FILETIME**構造を返します。 2つの入力パラメーターは変更されません。 **pwCarry**が NULL 以外の場合は、sum のキャリー結果 (0 または 1) を含みます。 
  
## <a name="remarks"></a>注釈

**ftadcft**関数は、 _pwCarry_が NULL の場合、 **ftaddft**と同じです。 _pwCarry_が NULL ではなく0をポイントしている場合、 **ftadcft**は**ftaddft**が返すのと同じ**FILETIME**値を返します。 
  
## <a name="see-also"></a>関連項目



[FtAddFt](ftaddft.md)

