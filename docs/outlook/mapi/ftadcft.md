---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f073dbb9655585ee56ab38be35bea4ef320042c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569772"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
キャリー フラグを使用して必要に応じて、別の 1 つの符号なし 64 ビット整数を追加します。
  
|||
|:-----|:-----|
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>パラメーター

 _ft1_
  
> [in]追加する最初の符号なし 64 ビット整数を格納する[FILETIME](filetime.md)構造体。 
    
 _ft2_
  
> [in]追加する 2 番目の符号なし 64 ビット整数を格納する FILETIME 構造体。
    
 _pwCarry_
  
> [in, out オプション]入力では、着信へのポインターは、フラグを実行します。 出力では、追加の実行結果へのポインター。 このパラメーターは、実行結果が必要でない場合、NULL にすることができます。
    
## <a name="return-value"></a>戻り値

**FtAdcFt**関数は、2 つの整数の合計を格納する**FILETIME**構造体を返します。 2 つの入力パラメーターは変更されません。 、合計の実行結果が含まれる**pwCarry**が NULL 以外の場合は、0 または 1 のいずれかです。 
  
## <a name="remarks"></a>注釈

_PwCarry_が NULL の場合に、 **FtAdcFt**関数を**FtAddFt**と同じです。 _PwCarry_が NULL でない場合は 0 ポイント、 **FtAdcFt**は、 **FtAddFt**を返す同じ**FILETIME**値を返します。 
  
## <a name="see-also"></a>関連項目



[FtAddFt](ftaddft.md)

