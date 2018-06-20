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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803789"
---
# <a name="rowentry"></a>ROWENTRY

**適用されます**: Outlook 
  
行および[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスを使用して、テーブルにその行に対して実行される操作が含まれています。 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>メンバー

**ulRowFlags**
  
> データに対して実行する次の操作のいずれかです。 
    
  - ROW_ADD: は、新しい行としてテーブルにデータを追加します。
      
  - ROW_MODIFY: は、テーブルの列を変更します。
      
  - ROW_REMOVE: は、この行をテーブルから削除します。
      
  - ROW_EMPTY: は、テーブルに行のデータを追加できません。 (行は空です)。
    
**あう**
  
> **RgPropvals**のプロパティの値の数。
    
**rgPropVals**
  
> [SPropValue](spropvalue.md)構造体をテーブルに挿入される列の値を表す配列。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |**ModifyTable**の後続のアクションを選択したルールの一覧を作成するために使用します。  <br/> |
   
## <a name="see-also"></a>関連項目
  
- [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
- [MAPI の構造](mapi-structures.md)

