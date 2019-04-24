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
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328008"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
符号なしの64ビットの整数をもう1つ追加します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>パラメーター

 _Addend1_
  
> 順番追加する最初の未署名の64ビット整数を含む[FILETIME](filetime.md)構造体。 
    
 _Addend2_
  
> 順番追加する2番目の符号なし64ビット整数を含む**FILETIME**構造。 
    
## <a name="return-value"></a>戻り値

**ftaddft**関数は、2つの整数の合計を含む**FILETIME**構造を返します。 2つの入力パラメーターは変更されません。 
  

