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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800442"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**適用されます**: Outlook 
  
MAPI テーブルのオブジェクトのインターフェイスへのポインターを返します。
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]予約されています。0 (ゼロ) にする必要があります。
    
ACLTABLE_FREEBUSY
  
> 新しい権限を設定します。
    
frightsFreeBusyDetailed
  
> ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の詳細を表示を提供します。
    
frightsFreeBusySimple
  
> ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の表示を提供します。
    
 _lppTable_
  
> [out]指す、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスは、テーブル オブジェクトが含まれています。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI では、 **IExchangeModifyTable::GetTable**メソッドを使用して、ルールのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

