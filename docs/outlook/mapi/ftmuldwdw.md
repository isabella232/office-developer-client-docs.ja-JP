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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592025"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  

