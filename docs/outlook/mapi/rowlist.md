---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b2e5255ef48fa90ce57e8b80d9e0a9214fca3f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624273"
---
# <a name="rowlist"></a>ROWLIST

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
行を表す [ROWENTRY](rowentry.md) 構造体の配列と [、IExchangeModifyTable](iexchangemodifytableiunknown.md) インターフェイスを介してテーブル内の行に対して実行される操作を格納します。 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>メンバー

 **cEntries**
  
> **aEntries** メンバーで指定された配列内のエントリの数。 
    
 **aEntries[MAPI_DIM]**
  
> 行と、テーブル内のそれらの行に対して実行される操作を含む **ROWENTRY** 構造体の配列。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |後続の ModifyTable アクションで選択したルールの一覧を **作成するために使用** します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI の構造](mapi-structures.md)

