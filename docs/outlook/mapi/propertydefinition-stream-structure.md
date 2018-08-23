---
title: PropertyDefinition ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b2de22eef455e59b7877524ce998e93a0a708e0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566657"
---
# <a name="propertydefinition-stream-structure"></a>PropertyDefinition ストリームの構造

**適用されます**: Outlook 2013 |Outlook 2016 
  
PropertyDefinition ストリームの構造体は、Microsoft Outlook アイテム内のすべてのユーザー定義フィールドの定義で、いくつかの組み込みのフィールドのデータ バインディングの設定を含む[FieldDefinition](fielddefinition-stream-structure.md)ストリームの構造体の配列です。 
  
PropertyDefinition ストリームの構造体をプログラムで操作できます。 ただし、Outlook のフォーム デザイナーを使用して同様の結果を達成することができ、データ バインド コントロールの**プロパティ**ダイアログ ボックスが具体的には、します。 
  
PropertyDefinition ストリームの構造体のフィールド定義には、2 つの形式のいずれかを指定できます: PropDefV1 と PropDefV2。 Outlook には、PropDefV1 と PropDefV2 の両方がサポートされています。 PropertyDefinition ストリームの構造体を 1 つですべてのフィールドの定義は、同じ形式でなければなりません。 PropDefV1 と PropDefV2 の違いの詳細については、 [FieldDefinition ストリームの構造体](fielddefinition-stream-structure.md)を参照してください。
  
このストリーム内のデータ要素は、以下に指定した順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。
  
- バージョン: ワード (2 バイト) を PropertyDefinition 内のフィールド定義の形式ストリームの構造体です。 次の表は、可能な値を示しています。
    
    |**値**|**説明**|
    |:-----|:-----|
    |0x0102  <br/> |形式は、PropDefV1 です。  <br/> |
    |0x0103  <br/> |形式は、PropDefV2 です。  <br/> |
   
- FieldDefinitionCount: DWORD (4 バイト) で、このストリーム内のフィールドの定義の数です。 これは、FieldDefinitions のデータ要素の配列の要素の数です。
    
- FieldDefinitions: FieldDefinition ストリームの構造体の配列。 この配列は、FieldDefinitionCount のデータ要素と同じです。
    
## <a name="see-also"></a>関連項目

- [Outlook のアイテムとフィールド](outlook-items-and-fields.md)
- [新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
- [ストリームの構造](stream-structures.md)

