---
title: ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581581"
---
# <a name="stream-structures"></a>ストリームの構造

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Outlook アイテムのユーザー定義のフィールドの定義は、 [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納されます。 このプロパティの値は、ユーザー定義フィールドと組み込みの Outlook アイテムのフィールドのデータ バインディングの設定の定義を格納するバイナリ ストリームです。 このセクションでは、ストリームの構造体を次に分割されて、バイナリ ストリームの構造に関する情報を提供します。 
  
> [!NOTE]
> これら (たとえば、PropertyDefinition、FieldDefinition、および SkipBlock) は、ストリームの構造とそのデータ要素の名前を選択し、プログラミング ・ インタ フェースの Messaging API (MAPI)、技術的には含まれていないドキュメントにのみ記載されて実際のストリームの構造体の目的。 開発者はこれらのアプリケーションでストリーム構造とデータ要素をラベル付けを選択する際です。 
  
- [PropertyDefinition ストリームの構造](propertydefinition-stream-structure.md)
    
- [FieldDefinition ストリームの構造](fielddefinition-stream-structure.md)
    
- [SkipBlock ストリームの構造](skipblock-stream-structure.md)
    
- [FirstSkipBlockContent ストリームの構造](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString ストリームの構造](packedansistring-stream-structure.md)
    
- [PackedUnicodeString ストリームの構造](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)

