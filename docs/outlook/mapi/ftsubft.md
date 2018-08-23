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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578263"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
別の 1 つの符号なし 64 ビット整数を減算します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>パラメーター

 _被減数_
  
> [in]減算される元となる_減数_パラメーターの値は、64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。 
    
 _減数_
  
> [in]_被減数_パラメーターで指定された値から減算する符号なし 64 ビット整数を格納する**FILETIME**構造体。 
    
## <a name="return-value"></a>戻り値

**FtSubFt**関数では、減算の結果を格納する**FILETIME**構造体を返します。 2 つの入力パラメーターは変更されません。 
  

