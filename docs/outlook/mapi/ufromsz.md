---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804173"
---
# <a name="ufromsz"></a>UFromSz

  
  
**適用されます**: Outlook 
  
以下の桁数、null で終わる文字列を符号なし整数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in]変換される null で終わる文字列へのポインター。 _Lpsz_パラメーターは、65536 文字を超えない必要があります。 
    
## <a name="return-value"></a>�߂�l

 **UFromSz**では、符号なし整数を返します。 文字列は、少なくとも 1 つの 10 進数字で始まらない、ゼロが返されます。 
  
## <a name="remarks"></a>備考

**UFromSz**関数では、10 進の数字ではない文字列の最初の文字に達したときの変換を停止します。 **UFromSz**は、「55」という文字列を指定するには、55 の整数値を返します。 文字列"5a5b"を指定するには、この関数は、整数値 5 を返します。 "A5b5"という文字列を指定するには、 **UFromSz**は 0 を返します。 
  
 **UFromSz**は、アクセントの違いに敏感です。 Unicode と DBCS の形式で文字列がサポートされています。 _Lpsz_の長さの制限は、文字数、バイト数ではありませんが。 
  
