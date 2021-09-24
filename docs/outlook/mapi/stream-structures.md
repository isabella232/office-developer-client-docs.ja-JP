---
title: Stream 構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 249910bcf29ca532359331fa712e8c3e65fd4a0d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549904"
---
# <a name="stream-structures"></a>Stream 構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムのユーザー定義フィールドの定義Outlook [PidLidPropertyDefinitionStream プロパティに格納](pidlidpropertydefinitionstream-canonical-property.md)されます。 このプロパティの値は、ユーザー定義フィールドの定義と、ユーザー定義アイテムの組み込みフィールドのデータ バインド設定を含むバイナリ ストリームOutlookです。 このセクションでは、バイナリ ストリームの構造に関する情報を以下のストリーム構造で説明します。 
  
> [!NOTE]
> これらのストリーム構造の名前 (PropertyDefinition、FieldDefinition、SkipBlock など) とそのデータ要素は、技術的にはメッセージング API (MAPI) のプログラミング インターフェイスの一部ではなく、実際のストリーム構造のドキュメント目的でのみ提供されます。 開発者は、選択したアプリケーションでこれらのストリーム構造とデータ要素にラベルを付けできます。 
  
- [PropertyDefinition ストリーム構造](propertydefinition-stream-structure.md)
    
- [FieldDefinition ストリーム構造](fielddefinition-stream-structure.md)
    
- [SkipBlock ストリーム構造](skipblock-stream-structure.md)
    
- [FirstSkipBlockContent ストリーム構造](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString ストリーム構造](packedansistring-stream-structure.md)
    
- [PackedUnicodeString ストリーム構造](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>関連項目



[Outlookアイテムとフィールド](outlook-items-and-fields.md)
  
[新しいフィールドの定義をUser-Definedする](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)

