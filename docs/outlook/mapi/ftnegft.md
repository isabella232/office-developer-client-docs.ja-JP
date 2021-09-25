---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c812cb081c1e4d86c0b3160066b6d953022560f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614172"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
符号なし 64 ビット整数の 2 の補数を計算します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>パラメーター

 _ft_
  
> [in] [2 つの](filetime.md) 補数を計算する符号なし 64 ビット整数を含む FILETIME 構造体。 
    
## <a name="return-value"></a>戻り値

**FtNegFt** 関数は、2 つの整数の補数を含む **FILETIME** 構造体を返します。 入力パラメーターは変更されません。 
  

