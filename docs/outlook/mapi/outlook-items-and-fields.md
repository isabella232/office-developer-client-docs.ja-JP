---
title: Outlookアイテムとフィールド
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
# <a name="outlook-items-and-fields"></a><span data-ttu-id="d4d34-103">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="d4d34-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="d4d34-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4d34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4d34-105">Microsoft Outlookは、機能に特化したアイテムの種類 (メール アイテム、予定、連絡先、タスク、メモなど) を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4d34-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="d4d34-106">Outlookは、一般に組み込みフィールドと呼ばれるアイテムの種類ごとに標準フィールドを提供します。</span><span class="sxs-lookup"><span data-stu-id="d4d34-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="d4d34-107">Outlookユーザー定義フィールドと呼ばれるユーザー設定フィールドを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="d4d34-108">各フィールドは、データ型と値に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="d4d34-109">データ型の例は **、通貨**、**日付/時刻**、**期間、\*\*\*\*整数**、**キーワード**、および **テキスト です**。</span><span class="sxs-lookup"><span data-stu-id="d4d34-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="d4d34-110">ユーザーは、フォーム デザイナーを使用してユーザー設定フィールドを定義Outlook。</span><span class="sxs-lookup"><span data-stu-id="d4d34-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="d4d34-111">プログラミング レベルでは、各アイテムは IMessage オブジェクト [によって表](imessageimapiprop.md) されます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="d4d34-112">各ユーザー定義フィールドは、フィールド定義と値に関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="d4d34-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="d4d34-113">フィールド定義</span><span class="sxs-lookup"><span data-stu-id="d4d34-113">Field Definition</span></span>

<span data-ttu-id="d4d34-114">フィールド定義には、名前、データ型、およびフィールドに関するその他の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="d4d34-115">各アイテムについて、Outlookは、対応する **IMessage** オブジェクトの [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティ内のすべてのユーザー定義フィールドの定義を格納します。</span><span class="sxs-lookup"><span data-stu-id="d4d34-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="d4d34-116">**PidLidPropertyDefinitionStream** プロパティには、フィールド定義を含む [PropertyDefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリ ストリームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="d4d34-117">フィールド定義のストリーム構造の詳細については [、「Stream Structures」を参照してください](stream-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="d4d34-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="d4d34-118">フィールド値</span><span class="sxs-lookup"><span data-stu-id="d4d34-118">Field Value</span></span>

<span data-ttu-id="d4d34-119">アイテムの各ユーザー定義フィールドには、対応する名前付きプロパティに格納される値があります。</span><span class="sxs-lookup"><span data-stu-id="d4d34-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="d4d34-120">この名前付きプロパティは、PS_PUBLIC_STRINGS セットに含まれます。プロパティ名には Unicode 文字文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="d4d34-121">プロパティのデータ型は、フィールドの種類に対応します。</span><span class="sxs-lookup"><span data-stu-id="d4d34-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="d4d34-122">プロパティが **IMessage** オブジェクトに存在しない場合、Outlookの既定値を前提とします。</span><span class="sxs-lookup"><span data-stu-id="d4d34-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="d4d34-123">たとえば、文字列型の場合、プロパティOutlook場合は空の文字列と見なされます。</span><span class="sxs-lookup"><span data-stu-id="d4d34-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4d34-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4d34-124">See also</span></span>



[<span data-ttu-id="d4d34-125">新しいフィールドの定義をUser-Definedする</span><span class="sxs-lookup"><span data-stu-id="d4d34-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="d4d34-126">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="d4d34-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="d4d34-127">Stream 構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="d4d34-128">PropertyDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="d4d34-129">FieldDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="d4d34-130">SkipBlock ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="d4d34-131">FirstSkipBlockContent ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="d4d34-132">PackedAnsiString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="d4d34-133">PackedUnicodeString ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="d4d34-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

