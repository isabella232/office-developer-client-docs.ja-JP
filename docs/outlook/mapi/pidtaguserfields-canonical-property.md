---
title: PidTagUserFields 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360740"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="3f577-103">PidTagUserFields 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3f577-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="3f577-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f577-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f577-105">ユーザー定義フィールドに関する名前、データ型、その他の情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3f577-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f577-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3f577-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f577-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="3f577-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="3f577-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3f577-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f577-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="3f577-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="3f577-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3f577-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f577-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f577-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3f577-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3f577-112">Area:</span></span>  <br/> |<span data-ttu-id="3f577-113">MAPI フォルダー</span><span class="sxs-lookup"><span data-stu-id="3f577-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f577-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3f577-114">Remarks</span></span>

<span data-ttu-id="3f577-115">各アイテムについて、Outlookは、対応する **IMessage** オブジェクトの [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティ内のすべてのユーザー定義フィールドの定義を格納します。</span><span class="sxs-lookup"><span data-stu-id="3f577-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="3f577-116">**PidLidPropertyDefinitionStream** プロパティには、フィールド定義を含む [PropertyDefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリ ストリームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f577-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="3f577-117">フィールド定義のストリーム構造の詳細については [、「Stream Structures」を参照してください](stream-structures.md)。</span><span class="sxs-lookup"><span data-stu-id="3f577-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="3f577-118">フォルダーごとに、Outlook は、そのフォルダー内のすべてのユーザー定義フィールドの定義を、メッセージ クラス IPC.MS の関連付けられたメッセージの **PidTagUserFields** プロパティに格納します。REN。USERFIELDS - 関連付けられたコンテンツ テーブルにこのクラスのメッセージが 1 つ以上含まれていると推定される各フォルダー。</span><span class="sxs-lookup"><span data-stu-id="3f577-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3f577-119">フォルダー内のユーザー定義フィールドのセットは、必ずしも各アイテムのユーザー定義フィールドのセットと一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3f577-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="3f577-120">フォルダー内のユーザー定義フィールドのセットは、フォルダーの Field Chooser など、Outlook UI のさまざまな場所に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f577-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="3f577-121">メッセージの **PidTagUserFields** プロパティには、フォルダー フィールド定義を含むバイナリ ストリーム **FolderUserFields** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f577-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="3f577-122">フォルダー フィールド定義のストリーム構造の詳細については [、「Folder Fields Stream Structures」](folder-fields-stream-structures.md) および [「FolderUserFields Stream Sample」を参照してください](folderuserfields-stream-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="3f577-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="3f577-123">セクション見出し</span><span class="sxs-lookup"><span data-stu-id="3f577-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3f577-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3f577-124">Protocol specifications</span></span>

<span data-ttu-id="3f577-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f577-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f577-126">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="3f577-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3f577-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3f577-127">Header files</span></span>

<span data-ttu-id="3f577-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f577-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f577-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f577-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f577-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f577-130">See also</span></span>



[<span data-ttu-id="3f577-131">Outlookアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="3f577-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="3f577-132">新しいフィールドの定義をUser-Definedする</span><span class="sxs-lookup"><span data-stu-id="3f577-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="3f577-133">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="3f577-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="3f577-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3f577-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f577-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3f577-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f577-136">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3f577-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f577-137">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3f577-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

