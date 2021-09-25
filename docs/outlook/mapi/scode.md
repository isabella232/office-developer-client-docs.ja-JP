---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 781d0a0485740f5f13175307a5d5c6939d7d71fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586762"
---
# <a name="scode"></a>SCODE

**適用対象**: Outlook 2013 | Outlook 2016 
  
エラーまたは警告を記述するために使用される 32 ビットの状態値。 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>注釈

**SCODE データ型** は [HRESULT](hresult.md)データ型と同じです。 
  
**SCODE 値は**、次の 4 つのフィールドに分かれています。 
  
- 成功を示すために 0 に設定され、失敗を示す 1 ビットの重大度コード。
    
- 11 ビット予約フィールド
    
- エラーまたは警告を担当する領域を示す 4 ビット機能コード。
    
- エラーまたは警告の原因となっている問題を説明する 16 ビット のエラーまたは警告コード。
    
MAPI 関数とメソッドの多くは、OLE メソッドと関数と同様に **、HRESULT** データ型として定義された **SCODE** 値を返します。 OLE は **、SCODE と HRESULT** の間の変換に使用できるいくつかの **マクロを定義します**。
  
> [!NOTE]
> 64 ビット MAPI では **、SCODE** は 32 ビット値です。 
  
MAPI で **SCODE** データ型を使用する方法の詳細については、「エラー処理」 [を参照してください](error-handling-in-mapi.md)。 OLE および **SCODE** データ型の詳細については  *、「OLE プログラマリファレンス」を参照してください*  。 
  
## <a name="see-also"></a>関連項目



[HRESULT 型](hresult.md)


[MAPI のデータ型](mapi-data-types.md)

