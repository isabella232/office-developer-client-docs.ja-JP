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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b02fc316001ae11d64988cc29d0e62e9adde55e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585585"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
別の 1 つの符号なし 64 ビット整数を追加します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>パラメーター

 _Addend1_
  
> [in]追加する最初の符号なし 64 ビット整数を格納する[FILETIME](filetime.md)構造体。 
    
 _Addend2_
  
> [in]追加する 2 番目の符号なし 64 ビット整数を格納する**FILETIME**構造体。 
    
## <a name="return-value"></a>戻り値

**FtAddFt**関数は、2 つの整数の合計を格納する**FILETIME**構造体を返します。 2 つの入力パラメーターは変更されません。 
  

