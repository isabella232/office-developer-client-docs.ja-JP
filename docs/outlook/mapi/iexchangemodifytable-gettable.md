---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 25a58769e464ec70bf859f09c7947b9861f16133
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561524"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI テーブル オブジェクトのインターフェイスへのポインターを返します。
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]予約済み。0 (ゼロ) である必要があります。
    
ACLTABLE_FREEBUSY
  
> 新しい権限を設定します。
    
frightsFreeBusyDetailed
  
> このACLTABLE_FREEBUSY、新しい空き時間情報の権限の詳細な表示を提供します。
    
frightsFreeBusySimple
  
> このACLTABLE_FREEBUSY、新しい空き時間情報の権限を簡単に表示します。
    
 _lppTable_
  
> [out] [IMAPITable : テーブル オブジェクトを含む IUnknown](imapitableiunknown.md) インターフェイスをポイントします。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI は **、IExchangeModifyTable::GetTable** メソッドを使用してルールのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

