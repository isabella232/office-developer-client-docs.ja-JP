---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 338f4336c0d229ccd5d336cdfdbd81f613be8848
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604951"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
バイナリ番号を 16 進数の文字列表現に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>パラメーター

 _pb_
  
> [in]変換するバイナリ データへのポインター。 
    
 _cb_
  
> [in]  _pb_ パラメーターが指すバイナリ データのサイズ (バイト単位)。 
    
 _sz_
  
> [out]バイナリ データを 16 進数で表す NULL 終端 ASCII 文字列へのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

**HexFromBin** 関数は、cb パラメーターによってサイズが示されるバイナリ データの単位へのポインター _を受け取_ ります。 sz 文字列(2* _cb_)+1 バイトのメモリ内で、このバイナリ情報を 16 進数で表します。 たとえば、バイト値が 10 進数の場合、16 進文字列は 0A になります。そのため、1 バイトは文字列内の 2 バイトに変換されます。 
  

