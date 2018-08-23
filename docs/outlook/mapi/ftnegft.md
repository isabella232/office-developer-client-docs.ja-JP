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
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589239"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
64 ビットの符号なし整数の 2 の補数を計算します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>パラメーター

 _ft_
  
> [in]2 の補数を計算する対象の 64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。 
    
## <a name="return-value"></a>戻り値

**FtNegFt**関数は、整数の 2 の補数を格納する**FILETIME**構造体を返します。 入力パラメーターは変更されません。 
  

