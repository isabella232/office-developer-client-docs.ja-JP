---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357499"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
16進数の文字列表現の指定した部分をバイナリ値に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> 順番変換する null で終わる文字列へのポインター。 有効な文字には、0 ~ 9 の16進文字、大文字、小文字の a ~ f があります。
    
 _pb_
  
> 読み上げ返されたバイナリ番号へのポインター。
    
 _cb_
  
> 順番_pb_パラメーターのサイズ (バイト単位)。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 変換に成功しました。
    
MAPI_E_CALL_FAILED
  
> 無効な文字が検出されました。
    
## <a name="see-also"></a>関連項目



[FBinFromHex](fbinfromhex.md)

