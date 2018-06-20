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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800236"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**適用されます**: Outlook 
  
2 進数を 16 進数の文字列形式に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parameters

 _pb_
  
> [in]変換するバイナリ データへのポインター。 
    
 _cb_
  
> [in]_Pb_パラメーターが指す、バイナリ データのバイト単位のサイズです。 
    
 _sz_
  
> [out]16 進数のバイナリ データを表す null で終わる ASCII 文字列へのポインター。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

**HexFromBin**関数は、バイナリ データのサイズが_cb_パラメーターで示される単位にポインターを受け取ります。 内_sz_文字列で返します (2 * _cb_) + 1 バイトのメモリ、16 進数のバイナリ情報を表したものです。 バイトの値が 10 進数の 10 の場合は、たとえば、16 進数の文字列になります 0 a、文字列内の 2 つのバイトは 1 バイトに変換。 
  

