---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336618"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI table オブジェクトのインターフェイスへのポインターを返します。
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番予約語0 (ゼロ) である必要があります。
    
ACLTABLE_FREEBUSY
  
> 新しい権限を設定します。
    
frightsFreeBusyDetailed
  
> ACLTABLE_FREEBUSY が渡されると、新しい空き時間情報の詳細が表示されます。
    
frightsFreeBusySimple
  
> ACLTABLE_FREEBUSY が渡されると、新しい空き時間情報が簡単に表示されます。
    
 _lpptable_
  
> 読み上げtable オブジェクトを含む[IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスを指します。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ルール  <br/> |crulesdlg:: onrefreshview  <br/> |mfcmapi は、 **IExchangeModifyTable:: GetTable**メソッドを使用してルールのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

