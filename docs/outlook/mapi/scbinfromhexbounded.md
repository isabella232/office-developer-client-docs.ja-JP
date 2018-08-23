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
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589281"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
16 進数の文字列形式の指定部分を 2 進数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>パラメーター

 _sz_
  
> [in]変換される null で終わる文字列へのポインター。 有効な文字には、9 との両方の大文字と小文字の文字を 16 進数の文字 0 ~ f が含まれます。
    
 _pb_
  
> [out]返される 2 進数へのポインター。
    
 _cb_
  
> [in]_Pb_パラメーターのバイト単位のサイズです。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 変換に成功しました。
    
MAPI_E_CALL_FAILED
  
> 無効な文字が発生しました。
    
## <a name="see-also"></a>関連項目



[FBinFromHex](fbinfromhex.md)

