---
title: 新しいユーザー定義フィールドの定義を追加する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428166"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>新しいユーザー定義フィールドの定義を追加する
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザー定義フィールドを Microsoft Outlookアイテムに追加すると、対応する[PropertyDefinition](propertydefinition-stream-structure.md)ストリーム構造にフィールド定義が追加されます。 PropertyDefinition ストリーム構造に新しいフィールド定義を追加するには、次の手順を実行します。 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>新しいユーザー定義フィールドの定義を追加するには

1. PropertyDefinition ストリーム構造の既存のフィールド定義を新しいフィールド定義配列にコピーします。 
    
2. 既存のフィールド定義が PropDefV1 形式の場合は、PropDefV2 形式に変換します。 フィールド定義形式の詳細については [、「PropertyDefinition Stream Structure」](propertydefinition-stream-structure.md) および [「FieldDefinition Stream Structure」を参照してください](fielddefinition-stream-structure.md)。
    
3. PropDefV2 形式の新しいユーザー定義フィールドの定義を作成し、それを配列に追加します。
    
4. Version 要素が値に設定されていない場合は、PropertyDefinition ストリーム構造の Version 要素を 0x0103として設定します。
    
5. FieldDefinitionCount 要素を 1 ずつインクリメントします。
    
6. 配列を FieldDefinitions 要素の値として格納します。
    
## <a name="see-also"></a>関連項目

- [PropertyDefinition ストリーム構造](propertydefinition-stream-structure.md)

