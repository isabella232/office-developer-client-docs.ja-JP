---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419185"
---
# <a name="rowlist"></a>ROWLIST

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブル内のこれらの行に対して実行される行と操作を表す[rowentry](rowentry.md)構造の配列が含まれています。 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>メンバー

 **centries**
  
> **aentries**メンバーによって指定された配列内のエントリの数。 
    
 **aentries [MAPI_DIM]**
  
> 行と、テーブル内のそれらの行に対して実行される操作を含む**rowentry**構造の配列。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ルール  <br/> |crulesdlg:: GetSelectedItems  <br/> |以降の**modifytable**アクションに対して選択されたルールの一覧を作成するために使用されます。  <br/> |
   
## <a name="see-also"></a>関連項目



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI の構造](mapi-structures.md)

