---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418177"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI テーブル オブジェクトを更新します。
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]次のいずれかの値を使用します。 
    
0 (ゼロ)
  
> ROWENTRY 構造体の **ulRowFlags** メンバー [の値を使用](rowentry.md) します。 
    
ACLTABLE_FREEBUSY
  
> 新しい権限を設定します。
    
frightsFreeBusyDetailed
  
> このACLTABLE_FREEBUSY、新しい空き時間情報の権限の詳細な表示を提供します。
    
frightsFreeBusySimple
  
> このACLTABLE_FREEBUSY、新しい空き時間情報の権限を簡単に表示します。
    
ROWLIST_REPLACE
  
> テーブル内のすべての行を置き換える。
    
 _lpMods_
  
> [in]テーブル オブジェクトのプロパティを含む [ROWLIST](rowlist.md) 構造体をポイントします。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI は **、IExchangeModifyTable::ModifyTable** メソッドを使用して、変更されたルールをルールのテーブルに書き戻します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

