---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327973"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
符号なしの64ビット整数の2つの補数を計算します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>パラメーター

 _cm_
  
> 順番2つの補数を計算するための符号なし64ビットの整数を含む[FILETIME](filetime.md)構造。 
    
## <a name="return-value"></a>戻り値

**FtNegFt**関数は、2の整数の補数を含む**FILETIME**構造体を返します。 入力パラメーターは変更されません。 
  

