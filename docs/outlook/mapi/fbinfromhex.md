---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800057"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**適用対象**: Outlook 
  
バイナリ データを 16 進数の文字列形式に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> [in]変換する null で終わる ASCII 文字列へのポインター。 Unicode 文字列ではありません。 有効な文字には、9 つと両方大文字と小文字の文字 A f を 16 進文字 0 にはが含まれます。
    
 _pb_
  
> [out]返される 2 進数へのポインター。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 文字列は、2 進数に正常に変換されました。 
    
FALSE 
  
> 入力文字列には、無効な ASCII 16 進数文字が含まれています。
    
## <a name="see-also"></a>関連項目



[ScBinFromHexBounded](scbinfromhexbounded.md)

