---
title: ROWLIST で
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803787"
---
# <a name="rowlist"></a>ROWLIST で

  
  
**適用されます**: Outlook 
  
行と[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブルの行に対して実行される操作を表す[ROWENTRY](rowentry.md)構造体の配列が含まれています。 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>メンバー

 **cEntries**
  
> **AEntries**メンバーによって指定された配列内のエントリの数です。 
    
 **aEntries [MAPI_DIM]**
  
> 行とテーブル内のこれらの行に対して実行される操作を含む**ROWENTRY**構造体の配列。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |**ModifyTable**の後続のアクションを選択したルールの一覧を作成するために使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)


[MAPI の構造](mapi-structures.md)

