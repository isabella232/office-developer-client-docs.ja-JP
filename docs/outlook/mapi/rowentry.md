---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436035"
---
# <a name="rowentry"></a>ROWENTRY

**適用対象**: Outlook 2013 | Outlook 2016 
  
[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを介してテーブル内のその行に対して実行される行と操作を格納します。 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Members

**ulRowFlags**
  
> データに対して実行する次のいずれかの操作。 
    
  - ROW_ADD: 新しい行としてテーブルにデータを追加します。
      
  - ROW_MODIFY: テーブル内のこの行を変更します。
      
  - ROW_REMOVE: テーブルからこの行を削除します。
      
  - ROW_EMPTY: 行データをテーブルに追加しない。 (行は空です)。
    
**cValues**
  
> **rgPropvals のプロパティ値の数** です。
    
**rgPropVals**
  
> テーブルに挿入する列の値を表す [SPropValue](spropvalue.md) 構造体の配列。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |後続の ModifyTable アクションで選択したルールの一覧を **作成するために使用** します。  <br/> |
   
## <a name="see-also"></a>関連項目
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [MAPI の構造](mapi-structures.md)

