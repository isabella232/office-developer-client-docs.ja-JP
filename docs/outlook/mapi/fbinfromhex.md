---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 021336f54d6ca7b00ee6ccb434edc91067075a15
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596464"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
16 進数の文字列表現をバイナリ データに変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> [in]変換する NULL 終端 ASCII 文字列へのポインター。 Unicode 文字列ではありません。 有効な文字には、0 から 9 の 16 進文字と、大文字と小文字の両方の文字 A から F が含まれます。
    
 _pb_
  
> [out]返されるバイナリ番号へのポインター。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 文字列はバイナリ番号に正常に変換されました。 
    
FALSE 
  
> 入力文字列に無効な ASCII 16 進文字が含まれています。
    
## <a name="see-also"></a>関連項目



[ScBinFromHexBounded](scbinfromhexbounded.md)

