---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404765"
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
  

