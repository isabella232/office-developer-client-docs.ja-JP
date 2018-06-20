---
title: Outlook アイテムおよびフィールド
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801706"
---
# <a name="outlook-items-and-fields"></a>Outlook アイテムおよびフィールド

  
  
**適用されます**: Outlook 
  
Microsoft Outlook には、(たとえば、メール アイテム、予定、連絡先、タスク、およびメモ) は、その機能に特化している項目の種類が用意されています。 Outlook では、一般的には組み込みのフィールドと呼ばれます、項目の種類ごとの標準フィールドが用意されています。 Outlook では、一般的にはユーザー定義フィールドと呼ばれます、カスタム フィールドを作成することもできます。 各フィールドは、データ型と値に関連付けられます。 データ型には、**通貨****日付/時刻**、**期間**、**整数**、**キーワード**、および**テキスト**があります。 ユーザーは、Outlook のフォーム デザイナーを使用してユーザー設定フィールドを定義できます。
  
プログラミング レベルでは、各項目は、 [IMessage](imessageimapiprop.md)オブジェクトによって表されます。 それぞれのユーザー定義フィールドは、フィールドの定義と値に関連付けられます。 
  
### <a name="field-definition"></a>フィールドの定義

フィールドの定義には、名前、データ型、およびフィールドの他の情報が含まれています。 、各項目については、Outlook は、対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティにユーザー定義のすべてのフィールドの定義を格納します。 **PidLidPropertyDefinitionStream**プロパティには、フィールド定義が含まれている[PropertyDefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリ ストリームが含まれています。 ストリームの構造体フィールドの定義の詳細については、[ストリームの構造](stream-structures.md)を参照してください。
  
### <a name="field-value"></a>フィールド値

各アイテムのユーザー定義のフィールドは、対応する名前付きプロパティに格納されている値を持ちます。 名前付きプロパティを PS_PUBLIC_STRINGS プロパティを設定するに、プロパティの名前と Unicode 文字の文字列です。 プロパティのデータ型は、フィールドの型に対応します。 **IMessage**オブジェクトのプロパティがない場合は、Outlook は、プロパティの適切な既定値を想定しています。 などの文字列タイプは、Outlook は空の文字列プロパティが存在しない場合。 
  
## <a name="see-also"></a>関連項目



[新しいユーザー定義フィールドの定義を追加します。](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[ストリームの構造](stream-structures.md)
  
[PropertyDefinition ストリームの構造](propertydefinition-stream-structure.md)
  
[FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)
  
[SkipBlock ストリームの構造](skipblock-stream-structure.md)
  
[FirstSkipBlockContent ストリームの構造](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString ストリームの構造](packedansistring-stream-structure.md)
  
[PackedUnicodeString ストリームの構造](packedunicodestring-stream-structure.md)

