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
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="6f851-103">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="6f851-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="6f851-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f851-105">ユーザー定義フィールドを Microsoft Outlookアイテムに追加すると、対応する[PropertyDefinition](propertydefinition-stream-structure.md)ストリーム構造にフィールド定義が追加されます。</span><span class="sxs-lookup"><span data-stu-id="6f851-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="6f851-106">PropertyDefinition ストリーム構造に新しいフィールド定義を追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6f851-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="6f851-107">新しいユーザー定義フィールドの定義を追加するには</span><span class="sxs-lookup"><span data-stu-id="6f851-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="6f851-108">PropertyDefinition ストリーム構造の既存のフィールド定義を新しいフィールド定義配列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="6f851-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="6f851-109">既存のフィールド定義が PropDefV1 形式の場合は、PropDefV2 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="6f851-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="6f851-110">フィールド定義形式の詳細については [、「PropertyDefinition Stream Structure」](propertydefinition-stream-structure.md) および [「FieldDefinition Stream Structure」を参照してください](fielddefinition-stream-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="6f851-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="6f851-111">PropDefV2 形式の新しいユーザー定義フィールドの定義を作成し、それを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="6f851-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="6f851-112">Version 要素が値に設定されていない場合は、PropertyDefinition ストリーム構造の Version 要素を 0x0103として設定します。</span><span class="sxs-lookup"><span data-stu-id="6f851-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="6f851-113">FieldDefinitionCount 要素を 1 ずつインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="6f851-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="6f851-114">配列を FieldDefinitions 要素の値として格納します。</span><span class="sxs-lookup"><span data-stu-id="6f851-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f851-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f851-115">See also</span></span>

- [<span data-ttu-id="6f851-116">PropertyDefinition ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="6f851-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

