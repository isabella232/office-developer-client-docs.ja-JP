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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414936"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
16進数値の文字列表現をバイナリデータに変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> 順番変換する null で終わる ASCII 文字列へのポインター。 Unicode 文字列ではありません。 有効な文字には、16進数の0から9までの文字、および大文字と小文字の両方が使用できます。
    
 _pb_
  
> 読み上げ返されたバイナリ番号へのポインター。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 文字列は、バイナリの数値に正しく変換されました。 
    
FALSE 
  
> 入力文字列に無効な ASCII 16 進文字が含まれています。
    
## <a name="see-also"></a>関連項目



[ScBinFromHexBounded](scbinfromhexbounded.md)

