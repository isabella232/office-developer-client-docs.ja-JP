---
title: Stream 構造体
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407824"
---
# <a name="stream-structures"></a><span data-ttu-id="f9277-103">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="f9277-103">Stream Structures</span></span>

  
  
<span data-ttu-id="f9277-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9277-105">Microsoft Outlook アイテムのユーザー定義フィールドの定義は、 [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="f9277-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="f9277-106">このプロパティの値は、Outlook アイテムの組み込みフィールドのユーザー定義フィールドおよびデータバインド設定の定義を含むバイナリストリームです。</span><span class="sxs-lookup"><span data-stu-id="f9277-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="f9277-107">このセクションでは、バイナリストリームの構造に関する情報を、次のストリーム構造で分けて説明します。</span><span class="sxs-lookup"><span data-stu-id="f9277-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f9277-108">これらの stream 構造体の名前 (propertydefinition、fielddefinition、および skipblock など) とそのデータ要素は、メッセージング API (MAPI) のプログラミングインターフェイスの一部ではありません。ここでは、ドキュメントにのみ記載されています。実際のストリーム構造の目的。</span><span class="sxs-lookup"><span data-stu-id="f9277-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="f9277-109">開発者は、ユーザーが選択したときに、これらの stream 構造体とデータ要素にラベルを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f9277-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="f9277-110">propertydefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="f9277-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="f9277-111">fielddefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="f9277-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="f9277-112">skipblock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="f9277-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="f9277-113">firstskipblockcontent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="f9277-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="f9277-114">PackedAnsiString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="f9277-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="f9277-115">PackedUnicodeString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="f9277-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="f9277-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9277-116">See also</span></span>



[<span data-ttu-id="f9277-117">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="f9277-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="f9277-118">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="f9277-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="f9277-119">propertydefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="f9277-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

