---
title: Stream 構造
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
# <a name="stream-structures"></a><span data-ttu-id="72548-103">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="72548-103">Stream Structures</span></span>

  
  
<span data-ttu-id="72548-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72548-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72548-105">アイテムのユーザー定義フィールドの定義Outlook [PidLidPropertyDefinitionStream プロパティに格納](pidlidpropertydefinitionstream-canonical-property.md)されます。</span><span class="sxs-lookup"><span data-stu-id="72548-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="72548-106">このプロパティの値は、ユーザー定義フィールドの定義と、ユーザー定義アイテムの組み込みフィールドのデータ バインド設定を含むバイナリ ストリームOutlookです。</span><span class="sxs-lookup"><span data-stu-id="72548-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="72548-107">このセクションでは、バイナリ ストリームの構造に関する情報を以下のストリーム構造で説明します。</span><span class="sxs-lookup"><span data-stu-id="72548-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="72548-108">これらのストリーム構造の名前 (PropertyDefinition、FieldDefinition、SkipBlock など) とそのデータ要素は、技術的にはメッセージング API (MAPI) のプログラミング インターフェイスの一部ではなく、実際のストリーム構造のドキュメント目的でのみ提供されます。</span><span class="sxs-lookup"><span data-stu-id="72548-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="72548-109">開発者は、選択したアプリケーションでこれらのストリーム構造とデータ要素にラベルを付けできます。</span><span class="sxs-lookup"><span data-stu-id="72548-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="72548-110">PropertyDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="72548-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="72548-111">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="72548-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="72548-112">SkipBlock ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="72548-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="72548-113">FirstSkipBlockContent ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="72548-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="72548-114">PackedAnsiString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="72548-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="72548-115">PackedUnicodeString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="72548-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="72548-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="72548-116">See also</span></span>



[<span data-ttu-id="72548-117">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="72548-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="72548-118">新しいフィールドの定義をUser-Definedする</span><span class="sxs-lookup"><span data-stu-id="72548-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="72548-119">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="72548-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

