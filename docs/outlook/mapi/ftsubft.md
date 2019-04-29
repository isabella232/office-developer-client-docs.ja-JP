---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408419"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つの符号なし64ビット整数を別の値に減算します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>パラメーター

 _Minuend_
  
> 順番_Subtrahend_パラメーターの値を減算する、符号なしの64ビットの整数を含む[FILETIME](filetime.md)構造。 
    
 _Subtrahend_
  
> 順番_Minuend_パラメーターによって指定された値から減算される、符号なしの64ビット整数を含む**FILETIME**構造。 
    
## <a name="return-value"></a>戻り値

**ftsubft**関数は、減算の結果を含む**FILETIME**構造を返します。 2つの入力パラメーターは変更されません。 
  

