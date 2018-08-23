---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800136"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**適用対象**: Outlook 
  
32 ビットの符号なし整数を符号なしの 64 ビット整数を乗算します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>パラメーター

 _べき乗_
  
> [in]マルチ プライアで 32 ビットの符号なし整数を含むダブル ワード。 
    
 _被乗数_
  
> [in]_乗数_パラメーターの値が乗算されます、64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。 
    
## <a name="return-value"></a>戻り値

**FtMulDw**関数は、2 つの整数の積を格納する**FILETIME**構造体を返します。 2 つの入力パラメーターは変更されません。 
  

