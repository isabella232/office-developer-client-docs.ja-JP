---
title: Outlook のアイテムとフィールド
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409119"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="dfdac-103">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="dfdac-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="dfdac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfdac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfdac-105">Microsoft Outlook では、その機能に特化したアイテムの種類 (メールアイテム、予定、連絡先、タスク、メモなど) を提供しています。</span><span class="sxs-lookup"><span data-stu-id="dfdac-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="dfdac-106">Outlook では、一般に組み込みフィールドと呼ばれる、アイテムの種類ごとに標準フィールドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="dfdac-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="dfdac-107">Outlook では、ユーザーがユーザー定義フィールドと呼ばれるユーザー設定フィールドを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="dfdac-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="dfdac-108">各フィールドは、データ型と値に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="dfdac-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="dfdac-109">データ型の例としては、**通貨**、**日付/時刻**、**期間**、**整数**、**キーワード**、**テキスト**などがあります。</span><span class="sxs-lookup"><span data-stu-id="dfdac-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="dfdac-110">ユーザーは、Outlook のフォームデザイナーを使用してユーザー設定フィールドを定義できます。</span><span class="sxs-lookup"><span data-stu-id="dfdac-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="dfdac-111">プログラミングレベルでは、各アイテムは[IMessage](imessageimapiprop.md)オブジェクトによって表されます。</span><span class="sxs-lookup"><span data-stu-id="dfdac-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="dfdac-112">各ユーザー定義フィールドは、フィールド定義と値に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="dfdac-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="dfdac-113">フィールド定義</span><span class="sxs-lookup"><span data-stu-id="dfdac-113">Field Definition</span></span>

<span data-ttu-id="dfdac-114">フィールド定義には、そのフィールドの名前、データ型、およびその他の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dfdac-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="dfdac-115">各アイテムについて、Outlook は、すべてのユーザー定義フィールドの定義を対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="dfdac-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="dfdac-116">**PidLidPropertyDefinitionStream**プロパティには、フィールド定義を含む[propertydefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dfdac-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="dfdac-117">フィールド定義のストリーム構造の詳細については、「 [stream 造](stream-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfdac-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="dfdac-118">フィールド値</span><span class="sxs-lookup"><span data-stu-id="dfdac-118">Field Value</span></span>

<span data-ttu-id="dfdac-119">アイテムの各ユーザー定義フィールドには、対応する名前付きプロパティに格納されている値があります。</span><span class="sxs-lookup"><span data-stu-id="dfdac-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="dfdac-120">その名前付きプロパティは PS_PUBLIC_STRINGS プロパティセットに含まれており、プロパティ名として Unicode 文字列を持ちます。</span><span class="sxs-lookup"><span data-stu-id="dfdac-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="dfdac-121">プロパティのデータ型は、フィールドの種類に対応します。</span><span class="sxs-lookup"><span data-stu-id="dfdac-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="dfdac-122">プロパティが**IMessage**オブジェクトに存在しない場合、Outlook はプロパティに対して適切な既定値を想定します。</span><span class="sxs-lookup"><span data-stu-id="dfdac-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="dfdac-123">たとえば、文字列型 (string) の場合、Outlook は、そのプロパティが存在しない場合は空の文字列を想定します。</span><span class="sxs-lookup"><span data-stu-id="dfdac-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfdac-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfdac-124">See also</span></span>



[<span data-ttu-id="dfdac-125">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="dfdac-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="dfdac-126">propertydefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="dfdac-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="dfdac-127">Stream 構造体</span><span class="sxs-lookup"><span data-stu-id="dfdac-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="dfdac-128">propertydefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="dfdac-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="dfdac-129">fielddefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="dfdac-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="dfdac-130">skipblock ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="dfdac-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="dfdac-131">firstskipblockcontent ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="dfdac-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="dfdac-132">PackedAnsiString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="dfdac-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="dfdac-133">PackedUnicodeString Stream 構造</span><span class="sxs-lookup"><span data-stu-id="dfdac-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

