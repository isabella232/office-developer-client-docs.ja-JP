---
title: PropertyDefinition ストリーム構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a0bf7e617b58da57c784d43156b73be8c2d6d520
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609655"
---
# <a name="propertydefinition-stream-structure"></a>PropertyDefinition ストリーム構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
PropertyDefinition ストリーム構造は、Microsoft Outlook アイテム内のすべてのユーザー定義フィールドの定義と、一部の組み込みフィールドのデータ バインド設定を含む[FieldDefinition](fielddefinition-stream-structure.md)ストリーム構造の配列です。 
  
PropertyDefinition ストリーム構造をプログラムで操作できます。 ただし、データ バインド コントロールの Outlookフォーム デザイナー、特に [プロパティ] ダイアログボックスを使用すると、同様の結果を得ることができます。 
  
PropertyDefinition ストリーム構造のフィールド定義には、PropDefV1 と PropDefV2 の 2 つの形式のいずれかを指定できます。 Outlook PropDefV1 と PropDefV2 の両方をサポートしています。 単一の PropertyDefinition ストリーム構造内のすべてのフィールド定義は、同じ形式である必要があります。 PropDefV1 と PropDefV2 の違いについて詳しくは [、「FieldDefinition ストリーム構造」をご覧ください](fielddefinition-stream-structure.md)。
  
このストリーム内のデータ要素は、リトル エンディアン バイト順に格納され、次に示す順序で互いに直後に格納されます。
  
- バージョン: WORD (2 バイト)、PropertyDefinition ストリーム構造内のフィールド定義の形式。 以下の表に使用できる値を示します。
    
    |**値**|**説明**|
    |:-----|:-----|
    |0x0102  <br/> |形式は PropDefV1 です。  <br/> |
    |0x0103  <br/> |形式は PropDefV2 です。  <br/> |
   
- FieldDefinitionCount: DWORD (4 バイト)、このストリーム内のフィールド定義の数。 これは、FieldDefinitions データ要素内の配列要素の数です。
    
- FieldDefinitions: FieldDefinition ストリーム構造の配列。 この配列の数は、FieldDefinitionCount データ要素と等しくなります。
    
## <a name="see-also"></a>関連項目

- [Outlookアイテムとフィールド](outlook-items-and-fields.md)
- [新しいフィールドの定義をUser-Definedする](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
- [Stream 構造](stream-structures.md)

