---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c50b658a956b1ccbaccafb707c9b60ffa13747f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610917"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つの符号なし 64 ビット整数を別の整数から減算します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>パラメーター

 _Minuend_
  
> [in]_Subtrahend_ パラメーターの値を減算する符号なし 64 ビット整数を含む [FILETIME](filetime.md)構造体。 
    
 _Subtrahend_
  
> [in]_Minuend_ パラメーターで示される値から減算された符号なし 64 ビット整数を含む **FILETIME** 構造体。 
    
## <a name="return-value"></a>戻り値

**FtSubFt** 関数は、減算の結果を含む **FILETIME** 構造体を返します。 2 つの入力パラメーターは変更されません。 
  

