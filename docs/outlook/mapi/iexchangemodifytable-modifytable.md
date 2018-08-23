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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800430"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**適用対象**: Outlook 
  
MAPI テーブルのオブジェクトを更新します。
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]次の値のいずれかを使用します。 
    
0 (ゼロ)
  
> **UlRowFlags** 、 [ROWENTRY](rowentry.md)構造体のメンバーの値を使用します。 
    
ACLTABLE_FREEBUSY
  
> 新しい権限を設定します。
    
frightsFreeBusyDetailed
  
> ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の詳細を表示を提供します。
    
frightsFreeBusySimple
  
> ACLTABLE_FREEBUSY が渡された場合は、新しい空き時間情報の権限の表示を提供します。
    
ROWLIST_REPLACE
  
> テーブル内のすべての行を交換してください。
    
 _lpMods_
  
> [in][Rowlist で](rowlist.md)を含む構造体のテーブルのオブジェクトのプロパティへのポインター。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI では、 **IExchangeModifyTable::ModifyTable**メソッドを使用して、変更したルールをルールのテーブルに書き込みます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

