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
  
ユーザー定義フィールドを Microsoft Outlook アイテムに追加するときは、対応する[propertydefinition](propertydefinition-stream-structure.md) stream 構造にフィールド定義を追加します。 次の手順を使用して、新しいフィールド定義を propertydefinition stream 構造に追加します。 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>新しいユーザー定義フィールドの定義を追加するには

1. propertydefinition stream 構造の既存のフィールド定義を新しいフィールド定義配列にコピーします。 
    
2. 既存のフィールド定義が PropDefV1 形式に設定されている場合は、それらを PropDefV2 形式に変換します。 フィールド定義の形式の詳細については、「 [propertydefinition stream 構造](propertydefinition-stream-structure.md)と[fielddefinition stream 構造](fielddefinition-stream-structure.md)」を参照してください。
    
3. PropDefV2 形式で新しいユーザー定義フィールドの定義を作成し、それを配列に追加します。
    
4. version 要素がこの値に設定されていない場合は、propertydefinition stream 構造の version 要素を0x0103 として設定します。
    
5. fielddefinitioncount 要素を1つずつインクリメントします。
    
6. 配列を fielddefinitions 要素の値として格納します。
    
## <a name="see-also"></a>関連項目

- [propertydefinition ストリームの構造](propertydefinition-stream-structure.md)

