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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430134"
---
# <a name="scode"></a>SCODE

**適用対象**: Outlook 2013 | Outlook 2016 
  
エラーまたは警告を記述するために使用される32ビットの状態の値。 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>注釈

**SCODE**データ型は、 [HRESULT](hresult.md)データ型と同じです。 
  
**SCODE**値は、次の4つのフィールドに分かれています。 
  
- 成功を示す0に設定されている1ビットの重大度コード。エラーを示す1を指定します。
    
- 11ビットの予約済みフィールド
    
- エラーまたは警告を担当する領域を示す4ビットのファシリティコード。
    
- エラーまたは警告を引き起こしている問題を説明する16ビットエラーまたは警告コード。
    
多くの MAPI の関数およびメソッドは、OLE のメソッドと関数として、 **HRESULT**データ型として定義された**SCODE**値を返します。 OLE は、 **SCODE**と**HRESULT**の間の変換に使用できるいくつかのマクロを定義します。
  
> [!NOTE]
> 64ビット MAPI では、 **SCODE**は32ビット値のままです。 
  
MAPI が**SCODE**データ型を使用する方法の詳細については、「[エラー処理](error-handling-in-mapi.md)」を参照してください。 ole および**SCODE**データ型の詳細については、「 *ole プログラマーズリファレンス*」を参照してください。 
  
## <a name="see-also"></a>関連項目



[HRESULT 型](hresult.md)


[MAPI のデータ型](mapi-data-types.md)

