---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f8ede3761ca10589c686e2ec4fac18fbe00fb2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588588"
---
# <a name="scode"></a>SCODE

**適用されます**: Outlook 2013 |Outlook 2016 
  
エラーまたは警告を記述するために使用される 32 ビットのステータス値です。 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>注釈

**データは、 [HRESULT](hresult.md)のデータ型と同じです。** 
  
**SCODE**の値は、4 つのフィールドに分かれています。 
  
- 返し、失敗を示すために 1 を 0 に設定されている単一のビットの重要度コードです。
    
- 11 ビットの予約フィールド
    
- 領域エラーまたは警告を担当することを示す 4 ビットの機能のコードです。
    
- 16 ビットのエラーまたは警告コード エラーまたは警告は、問題について説明します。
    
MAPI の関数およびメソッドの多くは、OLE メソッドと関数のように、 **HRESULT**のデータ型として定義されている**SCODE**の値を返します。 OLE は、 **SCODE**と**HRESULT**間の変換に使用できるいくつかのマクロを定義します。
  
> [!NOTE]
> 64 ビットの MAPI で**られません**が、32 ビット値です。 
  
MAPI が**SCODE**のデータ型を使用する方法の詳細については、[エラー処理](error-handling-in-mapi.md)を参照してください。 OLE および**SCODE**のデータ型の詳細については、 *OLE プログラマ リファレンス*を参照してください。 
  
## <a name="see-also"></a>関連項目



[HRESULT 型](hresult.md)


[MAPI データ型](mapi-data-types.md)

