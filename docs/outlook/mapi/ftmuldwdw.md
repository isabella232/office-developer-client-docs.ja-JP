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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800140"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**適用対象**: Outlook 
  
別の 1 つの符号なし 32 ビット整数を乗算します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>パラメーター

 _被乗数_
  
> [in]_乗数_パラメーターの値が乗算されます符号なし 32 ビット整数を含むダブル ワード。 
    
 _べき乗_
  
> [in]マルチ プライアで 32 ビットの符号なし整数を含むダブル ワード。
    
## <a name="return-value"></a>戻り値

**FtMulDwDw**関数は、2 つの整数の積を格納する[FILETIME](filetime.md)構造体を返します。 2 つの入力パラメーターは変更されません。 
  

