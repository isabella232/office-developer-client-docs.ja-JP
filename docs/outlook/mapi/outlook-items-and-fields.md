---
title: Outlook のアイテムとフィールド
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348546"
---
# <a name="outlook-items-and-fields"></a>Outlook のアイテムとフィールド

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook では、その機能に特化したアイテムの種類 (メールアイテム、予定、連絡先、タスク、メモなど) を提供しています。 Outlook では、一般に組み込みフィールドと呼ばれる、アイテムの種類ごとに標準フィールドが用意されています。 Outlook では、ユーザーがユーザー定義フィールドと呼ばれるユーザー設定フィールドを作成することもできます。 各フィールドは、データ型と値に関連付けられています。 データ型の例としては、**通貨**、**日付/時刻**、**期間**、**整数**、**キーワード**、**テキスト**などがあります。 ユーザーは、Outlook のフォームデザイナーを使用してユーザー設定フィールドを定義できます。
  
プログラミングレベルでは、各アイテムは[IMessage](imessageimapiprop.md)オブジェクトによって表されます。 各ユーザー定義フィールドは、フィールド定義と値に関連付けられています。 
  
### <a name="field-definition"></a>フィールド定義

フィールド定義には、そのフィールドの名前、データ型、およびその他の情報が含まれています。 各アイテムについて、Outlook は、すべてのユーザー定義フィールドの定義を対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納します。 **PidLidPropertyDefinitionStream**プロパティには、フィールド定義を含む[propertydefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリストリームが含まれています。 フィールド定義のストリーム構造の詳細については、「 [stream 造](stream-structures.md)」を参照してください。
  
### <a name="field-value"></a>フィールド値

アイテムの各ユーザー定義フィールドには、対応する名前付きプロパティに格納されている値があります。 その名前付きプロパティは PS_PUBLIC_STRINGS プロパティセットに含まれており、プロパティ名として Unicode 文字列を持ちます。 プロパティのデータ型は、フィールドの種類に対応します。 プロパティが**IMessage**オブジェクトに存在しない場合、Outlook はプロパティに対して適切な既定値を想定します。 たとえば、文字列型 (string) の場合、Outlook は、そのプロパティが存在しない場合は空の文字列を想定します。 
  
## <a name="see-also"></a>関連項目



[新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[propertydefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[Stream 構造体](stream-structures.md)
  
[propertydefinition ストリームの構造](propertydefinition-stream-structure.md)
  
[fielddefinition ストリームの構造](fielddefinition-stream-structure.md)
  
[skipblock ストリームの構造](skipblock-stream-structure.md)
  
[firstskipblockcontent ストリームの構造](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString Stream 構造](packedansistring-stream-structure.md)
  
[PackedUnicodeString Stream 構造](packedunicodestring-stream-structure.md)

