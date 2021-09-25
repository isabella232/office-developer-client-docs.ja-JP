---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 36b5a8754d1cf111a84e9b0e442ca5ab3c4afcf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576248"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つの符号なし 64 ビット整数を別の整数に追加します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>パラメーター

 _Addend1_
  
> [in]追加 [する最初](filetime.md) の符号なし 64 ビット整数を含む FILETIME 構造体。 
    
 _Addend2_
  
> [in]追加 **する 2** 番目の符号なし 64 ビット整数を含む FILETIME 構造体。 
    
## <a name="return-value"></a>戻り値

**FtAddFt** 関数は、2 つの整数の合計を含む **FILETIME** 構造体を返します。 2 つの入力パラメーターは変更されません。 
  

