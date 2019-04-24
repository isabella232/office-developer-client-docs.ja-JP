---
title: propertydefinition ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328484"
---
# <a name="propertydefinition-stream-structure"></a>propertydefinition ストリームの構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
propertydefinition ストリーム構造は、Microsoft Outlook アイテムのすべてのユーザー定義フィールドの定義と、いくつかの組み込みフィールドのデータバインド設定を含む[fielddefinition](fielddefinition-stream-structure.md) stream 構造の配列です。 
  
プログラムを使用して、propertydefinition ストリームの構造を操作できます。 ただし、Outlook フォームデザイナーおよび特に、データ連結コントロールの [**プロパティ**] ダイアログボックスを使用して、同様の結果を得ることができます。 
  
propertydefinition stream 構造のフィールド定義は、PropDefV1 と PropDefV2 の2つの形式のいずれかにすることができます。 Outlook では、PropDefV1 と PropDefV2 の両方をサポートしています。 単一の propertydefinition stream 構造のすべてのフィールド定義は、同じ形式でなければなりません。 PropDefV1 と PropDefV2 の相違点の詳細については、「 [fielddefinition Stream Structure](fielddefinition-stream-structure.md)」を参照してください。
  
このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。
  
- バージョン: WORD (2 バイト)。 propertydefinition stream 構造のフィールド定義の形式です。 以下の表に使用できる値を示します。
    
    |**値**|**説明**|
    |:-----|:-----|
    |0x0102  <br/> |形式は PropDefV1 です。  <br/> |
    |0x0103  <br/> |形式は PropDefV2 です。  <br/> |
   
- fielddefinitioncount: このストリーム内のフィールド定義の数である DWORD (4 バイト)。 fielddefinitions data 要素の配列要素の数を示します。
    
- fielddefinitions: fielddefinitions ストリーム構造の配列。 この配列の数は、fielddefinitioncount data 要素と同じです。
    
## <a name="see-also"></a>関連項目

- [Outlook のアイテムとフィールド](outlook-items-and-fields.md)
- [新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [propertydefinition ストリームのサンプル](propertydefinition-stream-sample.md)
- [Stream 構造体](stream-structures.md)

