---
title: 新しいユーザー定義フィールドの定義を追加します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592718"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>新しいユーザー定義フィールドの定義を追加します。
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
Microsoft Outlook アイテムにユーザー定義フィールドを追加するときは、 [PropertyDefinition](propertydefinition-stream-structure.md)ストリームの対応する構造体にフィールドの定義を追加します。 PropertyDefinition ストリームの構造体への新しいフィールド定義を追加するのにには、次の手順を使用します。 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>新しいユーザー定義のフィールドの定義を追加するのには

1. PropertyDefinition ストリームの構造体のフィールドの既存の定義を新しいフィールド定義の配列にコピーします。 
    
2. PropDefV1 形式で、既存のフィールドの定義がある場合は、PropDefV2 の形式に変換します。 フィールド定義の書式の詳細については、 [PropertyDefinition ストリームの構造体](propertydefinition-stream-structure.md)および[FieldDefinition ストリームの構造体](fielddefinition-stream-structure.md)を参照してください。
    
3. PropDefV2 の形式で新しいユーザー定義フィールドの定義を作成し、配列に追加します。
    
4. バージョン要素がその値に設定されていない場合は、0x0103、として、バージョン、PropertyDefinition ストリーム構造体の要素を設定します。
    
5. FieldDefinitionCount 要素は、1 ずつ増加します。
    
6. FieldDefinitions 要素の値として配列を格納します。
    
## <a name="see-also"></a>関連項目

- [PropertyDefinition ストリームの構造](propertydefinition-stream-structure.md)

