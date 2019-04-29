---
title: 新しいユーザー定義フィールドの定義を追加する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428166"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="a723f-103">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="a723f-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="a723f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a723f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a723f-105">ユーザー定義フィールドを Microsoft Outlook アイテムに追加するときは、対応する[propertydefinition](propertydefinition-stream-structure.md) stream 構造にフィールド定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="a723f-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="a723f-106">次の手順を使用して、新しいフィールド定義を propertydefinition stream 構造に追加します。</span><span class="sxs-lookup"><span data-stu-id="a723f-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="a723f-107">新しいユーザー定義フィールドの定義を追加するには</span><span class="sxs-lookup"><span data-stu-id="a723f-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="a723f-108">propertydefinition stream 構造の既存のフィールド定義を新しいフィールド定義配列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="a723f-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="a723f-109">既存のフィールド定義が PropDefV1 形式に設定されている場合は、それらを PropDefV2 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="a723f-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="a723f-110">フィールド定義の形式の詳細については、「 [propertydefinition stream 構造](propertydefinition-stream-structure.md)と[fielddefinition stream 構造](fielddefinition-stream-structure.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a723f-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="a723f-111">PropDefV2 形式で新しいユーザー定義フィールドの定義を作成し、それを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="a723f-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="a723f-112">version 要素がこの値に設定されていない場合は、propertydefinition stream 構造の version 要素を0x0103 として設定します。</span><span class="sxs-lookup"><span data-stu-id="a723f-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="a723f-113">fielddefinitioncount 要素を1つずつインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="a723f-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="a723f-114">配列を fielddefinitions 要素の値として格納します。</span><span class="sxs-lookup"><span data-stu-id="a723f-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a723f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a723f-115">See also</span></span>

- [<span data-ttu-id="a723f-116">propertydefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="a723f-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

