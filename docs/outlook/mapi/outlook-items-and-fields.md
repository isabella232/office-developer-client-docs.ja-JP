---
title: Outlookアイテムとフィールド
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b33f42e4203afeaa5d2f14bc46c84e8db060c468
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584004"
---
# <a name="outlook-items-and-fields"></a>Outlookアイテムとフィールド

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlookは、機能に特化したアイテムの種類 (メール アイテム、予定、連絡先、タスク、メモなど) を提供します。 Outlookは、一般に組み込みフィールドと呼ばれるアイテムの種類ごとに標準フィールドを提供します。 Outlookユーザー定義フィールドと呼ばれるユーザー設定フィールドを作成することもできます。 各フィールドは、データ型と値に関連付けます。 データ型の例は **、通貨**、**日付/時刻**、**期間、****整数**、**キーワード**、および **テキスト です**。 ユーザーは、フォーム デザイナーを使用してユーザー設定フィールドを定義Outlook。
  
プログラミング レベルでは、各アイテムは IMessage オブジェクト [によって表](imessageimapiprop.md) されます。 各ユーザー定義フィールドは、フィールド定義と値に関連付けられる。 
  
### <a name="field-definition"></a>フィールド定義

フィールド定義には、名前、データ型、およびフィールドに関するその他の情報が含まれます。 各アイテムについて、Outlookは、対応する **IMessage** オブジェクトの [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティ内のすべてのユーザー定義フィールドの定義を格納します。 **PidLidPropertyDefinitionStream** プロパティには、フィールド定義を含む [PropertyDefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリ ストリームが含まれます。 フィールド定義のストリーム構造の詳細については [、「Stream Structures」を参照してください](stream-structures.md)。
  
### <a name="field-value"></a>フィールド値

アイテムの各ユーザー定義フィールドには、対応する名前付きプロパティに格納される値があります。 この名前付きプロパティは、PS_PUBLIC_STRINGS セットに含まれます。プロパティ名には Unicode 文字文字列が含まれます。 プロパティのデータ型は、フィールドの種類に対応します。 プロパティが **IMessage** オブジェクトに存在しない場合、Outlookの既定値を前提とします。 たとえば、文字列型の場合、プロパティOutlook場合は空の文字列と見なされます。 
  
## <a name="see-also"></a>関連項目



[新しいフィールドの定義をUser-Definedする](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[Stream 構造](stream-structures.md)
  
[PropertyDefinition ストリーム構造](propertydefinition-stream-structure.md)
  
[FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)
  
[SkipBlock ストリーム構造](skipblock-stream-structure.md)
  
[FirstSkipBlockContent ストリーム構造](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString ストリーム構造](packedansistring-stream-structure.md)
  
[PackedUnicodeString ストリーム構造](packedunicodestring-stream-structure.md)

