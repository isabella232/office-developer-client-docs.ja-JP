---
title: 新しいユーザー定義フィールドの定義を追加します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800211"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="38d26-103">新しいユーザー定義フィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="38d26-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="38d26-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38d26-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38d26-105">Microsoft Outlook アイテムにユーザー定義フィールドを追加するときは、 [PropertyDefinition](propertydefinition-stream-structure.md)ストリームの対応する構造体にフィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="38d26-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="38d26-106">PropertyDefinition ストリームの構造体への新しいフィールド定義を追加するのにには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="38d26-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="38d26-107">新しいユーザー定義のフィールドの定義を追加するのには</span><span class="sxs-lookup"><span data-stu-id="38d26-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="38d26-108">PropertyDefinition ストリームの構造体のフィールドの既存の定義を新しいフィールド定義の配列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="38d26-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="38d26-109">PropDefV1 形式で、既存のフィールドの定義がある場合は、PropDefV2 の形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="38d26-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="38d26-110">フィールド定義の書式の詳細については、 [PropertyDefinition ストリームの構造体](propertydefinition-stream-structure.md)および[FieldDefinition ストリームの構造体](fielddefinition-stream-structure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38d26-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="38d26-111">PropDefV2 の形式で新しいユーザー定義フィールドの定義を作成し、配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="38d26-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="38d26-112">バージョン要素がその値に設定されていない場合は、0x0103、として、バージョン、PropertyDefinition ストリーム構造体の要素を設定します。</span><span class="sxs-lookup"><span data-stu-id="38d26-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="38d26-113">FieldDefinitionCount 要素は、1 ずつ増加します。</span><span class="sxs-lookup"><span data-stu-id="38d26-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="38d26-114">FieldDefinitions 要素の値として配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="38d26-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38d26-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="38d26-115">See also</span></span>

- [<span data-ttu-id="38d26-116">PropertyDefinition ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="38d26-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

