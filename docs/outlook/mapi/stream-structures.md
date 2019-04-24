---
title: Stream 構造体
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327441"
---
# <a name="stream-structures"></a>Stream 構造体

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook アイテムのユーザー定義フィールドの定義は、 [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納されます。 このプロパティの値は、Outlook アイテムの組み込みフィールドのユーザー定義フィールドおよびデータバインド設定の定義を含むバイナリストリームです。 このセクションでは、バイナリストリームの構造に関する情報を、次のストリーム構造で分けて説明します。 
  
> [!NOTE]
> これらの stream 構造体の名前 (propertydefinition、fielddefinition、および skipblock など) とそのデータ要素は、メッセージング API (MAPI) のプログラミングインターフェイスの一部ではありません。ここでは、ドキュメントにのみ記載されています。実際のストリーム構造の目的。 開発者は、ユーザーが選択したときに、これらの stream 構造体とデータ要素にラベルを付けることができます。 
  
- [propertydefinition ストリームの構造](propertydefinition-stream-structure.md)
    
- [fielddefinition ストリームの構造](fielddefinition-stream-structure.md)
    
- [skipblock ストリームの構造](skipblock-stream-structure.md)
    
- [firstskipblockcontent ストリームの構造](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString Stream 構造](packedansistring-stream-structure.md)
    
- [PackedUnicodeString Stream 構造](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[propertydefinition ストリームのサンプル](propertydefinition-stream-sample.md)

