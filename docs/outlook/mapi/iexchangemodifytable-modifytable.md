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
  
MAPI テーブルオブジェクトを更新します。
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番次のいずれかの値を使用します。 
    
0 (ゼロ)
  
> [rowentry](rowentry.md)構造の**ulrowflags**メンバーの値を使用します。 
    
ACLTABLE_FREEBUSY
  
> 新しい権限を設定します。
    
frightsFreeBusyDetailed
  
> ACLTABLE_FREEBUSY が渡されると、新しい空き時間情報の詳細が表示されます。
    
frightsFreeBusySimple
  
> ACLTABLE_FREEBUSY が渡されると、新しい空き時間情報が簡単に表示されます。
    
ROWLIST_REPLACE
  
> 表のすべての行を置き換えます。
    
 _lpMods_
  
> 順番table オブジェクトのプロパティを含む[rowlist](rowlist.md)構造体を指します。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ルール  <br/> |crulesdlg:: OnModifySelectedItem  <br/> |mfcmapi は、 **IExchangeModifyTable:: modifytable**メソッドを使用して、変更されたルールをルールのテーブルに書き戻します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

