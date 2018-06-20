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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800143"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _Addend1_
  
> [in]追加する最初の符号なし 64 ビット整数を格納する[FILETIME](filetime.md)構造体。 
    
 _Addend2_
  
> [in]追加する 2 番目の符号なし 64 ビット整数を格納する**FILETIME**構造体。 
    
## <a name="return-value"></a>�߂�l

**FtAddFt**関数は、2 つの整数の合計を格納する**FILETIME**構造体を返します。 2 つの入力パラメーターは変更されません。 
  

