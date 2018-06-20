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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800151"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _ft_
  
> [in]2 の補数を計算する対象の 64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。 
    
## <a name="return-value"></a>�߂�l

**FtNegFt**関数は、整数の 2 の補数を格納する**FILETIME**構造体を返します。 入力パラメーターは変更されません。 
  

