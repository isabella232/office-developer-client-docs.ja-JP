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
  
1 つの符号なし 32 ビット整数を別の整数で乗算します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>パラメーター

 _Multiplicand_
  
> [in]Multiplier パラメーターの値を乗算する符号なし 32 ビット整数を含む 2 つの  _単語_ 。 
    
 _べき乗_
  
> [in]符号なし 32 ビット整数乗数を含む 2 つの単語。
    
## <a name="return-value"></a>戻り値

**FtMulDwDw** 関数は、2 つの整数の製品を含む [FILETIME](filetime.md)構造体を返します。 2 つの入力パラメーターは変更されません。 
  

