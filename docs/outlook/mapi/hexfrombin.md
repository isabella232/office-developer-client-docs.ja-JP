---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412577"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
バイナリ番号を16進数の文字列表現に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>パラメーター

 _pb_
  
> 順番変換するバイナリデータへのポインター。 
    
 _cb_
  
> 順番_pb_パラメーターが指すバイナリデータのサイズ (バイト数)。 
    
 _sz_
  
> 読み上げバイナリデータを16進数で表す null で終わる ASCII 文字列へのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

**HexFromBin**関数は、 _cb_パラメーターで指定されたサイズを持つバイナリデータの単位へのポインターを受け取ります。 これは、(2 * _cb_) + 1 バイトのメモリ内で、このバイナリ情報を16進数で表した_sz_文字列で返されます。 たとえば、バイト値が10進数の10の場合、16進文字列は0a になり、1バイトが文字列の2バイトに変換されます。 
  

