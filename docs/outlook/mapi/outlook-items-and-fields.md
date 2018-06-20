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
# <a name="outlook-items-and-fields"></a><span data-ttu-id="fe315-103">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="fe315-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="fe315-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe315-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe315-105">Microsoft Outlook には、(たとえば、メール アイテム、予定、連絡先、タスク、およびメモ) は、その機能に特化している項目の種類が用意されています。</span><span class="sxs-lookup"><span data-stu-id="fe315-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="fe315-106">Outlook では、一般的には組み込みのフィールドと呼ばれます、項目の種類ごとの標準フィールドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="fe315-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="fe315-107">Outlook では、一般的にはユーザー定義フィールドと呼ばれます、カスタム フィールドを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe315-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="fe315-108">各フィールドは、データ型と値に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="fe315-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="fe315-109">データ型には、**通貨****日付/時刻**、**期間**、**整数**、**キーワード**、および**テキスト**があります。</span><span class="sxs-lookup"><span data-stu-id="fe315-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="fe315-110">ユーザーは、Outlook のフォーム デザイナーを使用してユーザー設定フィールドを定義できます。</span><span class="sxs-lookup"><span data-stu-id="fe315-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="fe315-111">プログラミング レベルでは、各項目は、 [IMessage](imessageimapiprop.md)オブジェクトによって表されます。</span><span class="sxs-lookup"><span data-stu-id="fe315-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="fe315-112">それぞれのユーザー定義フィールドは、フィールドの定義と値に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="fe315-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="fe315-113">フィールドの定義</span><span class="sxs-lookup"><span data-stu-id="fe315-113">Field Definition</span></span>

<span data-ttu-id="fe315-114">フィールドの定義には、名前、データ型、およびフィールドの他の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe315-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="fe315-115">、各項目については、Outlook は、対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティにユーザー定義のすべてのフィールドの定義を格納します。</span><span class="sxs-lookup"><span data-stu-id="fe315-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="fe315-116">**PidLidPropertyDefinitionStream**プロパティには、フィールド定義が含まれている[PropertyDefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリ ストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe315-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="fe315-117">ストリームの構造体フィールドの定義の詳細については、[ストリームの構造](stream-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe315-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="fe315-118">フィールド値</span><span class="sxs-lookup"><span data-stu-id="fe315-118">Field Value</span></span>

<span data-ttu-id="fe315-119">各アイテムのユーザー定義のフィールドは、対応する名前付きプロパティに格納されている値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="fe315-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="fe315-120">名前付きプロパティを PS_PUBLIC_STRINGS プロパティを設定するに、プロパティの名前と Unicode 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="fe315-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="fe315-121">プロパティのデータ型は、フィールドの型に対応します。</span><span class="sxs-lookup"><span data-stu-id="fe315-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="fe315-122">**IMessage**オブジェクトのプロパティがない場合は、Outlook は、プロパティの適切な既定値を想定しています。</span><span class="sxs-lookup"><span data-stu-id="fe315-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="fe315-123">などの文字列タイプは、Outlook は空の文字列プロパティが存在しない場合。</span><span class="sxs-lookup"><span data-stu-id="fe315-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe315-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe315-124">See also</span></span>



[<span data-ttu-id="fe315-125">新しいユーザー定義フィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe315-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="fe315-126">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="fe315-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="fe315-127">ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="fe315-128">PropertyDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="fe315-129">FieldDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="fe315-130">SkipBlock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="fe315-131">FirstSkipBlockContent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="fe315-132">PackedAnsiString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="fe315-133">PackedUnicodeString ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="fe315-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

