---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c1e37da677fa38eb83a22db0c170eb6dd45cb8be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561762"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
必要に応じて、キャリー フラグを使用して、1 つの符号なし 64 ビット整数を別の整数に追加します。
  
|||
|:-----|:-----|
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>パラメーター

 _ft1_
  
> [in]追加 [する最初](filetime.md) の符号なし 64 ビット整数を含む FILETIME 構造体。 
    
 _ft2_
  
> [in]追加する 2 番目の符号なし 64 ビット整数を含む FILETIME 構造体。
    
 _pwCarry_
  
> [in, out, optional]入力時に、受信キャリー フラグへのポインター。 出力時に、加算のキャリー結果へのポインター。 キャリー結果が不要な場合、このパラメーターは NULL に設定できます。
    
## <a name="return-value"></a>戻り値

**FtAdcFt** 関数は、2 つの整数の合計を含む **FILETIME** 構造体を返します。 2 つの入力パラメーターは変更されません。 **pwCarry が** NULL 以外の場合、合計のキャリー結果 (0 または 1) が含まれる。 
  
## <a name="remarks"></a>注釈

PwCarry が NULL の場合 **、FtAdcFt** 関数は **FtAddFt**  _と_ 同じです。 _pwCarry が_ NULL ではなく、0 をポイントする場合 **、FtAdcFt** は **FtAddFt** が返すのと同じ **FILETIME** 値を返します。 
  
## <a name="see-also"></a>関連項目



[FtAddFt](ftaddft.md)

