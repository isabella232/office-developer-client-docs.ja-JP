---
title: ストリームの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804021"
---
# <a name="stream-structures"></a><span data-ttu-id="cd11a-103">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-103">Stream Structures</span></span>

  
  
<span data-ttu-id="cd11a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cd11a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cd11a-105">Outlook アイテムのユーザー定義のフィールドの定義は、 [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="cd11a-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="cd11a-106">このプロパティの値は、ユーザー定義フィールドと組み込みの Outlook アイテムのフィールドのデータ バインディングの設定の定義を格納するバイナリ ストリームです。</span><span class="sxs-lookup"><span data-stu-id="cd11a-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="cd11a-107">このセクションでは、ストリームの構造体を次に分割されて、バイナリ ストリームの構造に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cd11a-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cd11a-108">これら (たとえば、PropertyDefinition、FieldDefinition、および SkipBlock) は、ストリームの構造とそのデータ要素の名前を選択し、プログラミング ・ インタ フェースの Messaging API (MAPI)、技術的には含まれていないドキュメントにのみ記載されて実際のストリームの構造体の目的。</span><span class="sxs-lookup"><span data-stu-id="cd11a-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="cd11a-109">開発者はこれらのアプリケーションでストリーム構造とデータ要素をラベル付けを選択する際です。</span><span class="sxs-lookup"><span data-stu-id="cd11a-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="cd11a-110">PropertyDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="cd11a-111">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="cd11a-112">SkipBlock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="cd11a-113">FirstSkipBlockContent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="cd11a-114">PackedAnsiString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="cd11a-115">PackedUnicodeString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="cd11a-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="cd11a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd11a-116">See also</span></span>



[<span data-ttu-id="cd11a-117">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="cd11a-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="cd11a-118">新しいユーザー定義フィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="cd11a-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="cd11a-119">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="cd11a-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

