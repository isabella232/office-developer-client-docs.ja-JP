---
title: PidTagUserFields 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360740"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="8a6a8-103">PidTagUserFields 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a6a8-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="8a6a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a6a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a6a8-105">ユーザー定義フィールドの名前、データ型、およびその他の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a6a8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8a6a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a6a8-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="8a6a8-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="8a6a8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8a6a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a6a8-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="8a6a8-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="8a6a8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8a6a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a6a8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a6a8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a6a8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8a6a8-112">Area:</span></span>  <br/> |<span data-ttu-id="8a6a8-113">MAPI フォルダー</span><span class="sxs-lookup"><span data-stu-id="8a6a8-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a6a8-114">解説</span><span class="sxs-lookup"><span data-stu-id="8a6a8-114">Remarks</span></span>

<span data-ttu-id="8a6a8-115">各アイテムについて、Outlook は、すべてのユーザー定義フィールドの定義を対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="8a6a8-116">**PidLidPropertyDefinitionStream**プロパティには、フィールド定義を含む[propertydefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="8a6a8-117">フィールド定義のストリーム構造の詳細については、「 [stream 造](stream-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="8a6a8-118">各フォルダーについて、Outlook は、メッセージクラス IPC.MS の関連付けられたメッセージの**PidTagUserFields**プロパティに、そのフォルダー内のすべてのユーザー定義フィールドの定義を格納します。REN.userfields-各フォルダーは、関連付けられた contents テーブルにこのクラスのメッセージを1つだけ含めることを想定していました。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8a6a8-119">フォルダー内のユーザー定義フィールドのセットは、各アイテムのユーザー定義フィールドのセットと必ずしも一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="8a6a8-120">フォルダー内のユーザー定義フィールドのセットは、フォルダーの [フィールドの選択] など、Outlook UI 内のさまざまな場所に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="8a6a8-121">メッセージの**PidTagUserFields**プロパティには、フォルダーフィールドの定義を含むバイナリストリーム、 **folderuserfields**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="8a6a8-122">フォルダーフィールド定義のストリーム構造の詳細については、「 [folder Fields stream 構造](folder-fields-stream-structures.md)」および「 [folderuserfields stream Sample](folderuserfields-stream-sample.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="8a6a8-123">セクション見出し</span><span class="sxs-lookup"><span data-stu-id="8a6a8-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a6a8-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8a6a8-124">Protocol specifications</span></span>

<span data-ttu-id="8a6a8-125">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a6a8-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a6a8-126">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a6a8-127">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8a6a8-127">Header files</span></span>

<span data-ttu-id="8a6a8-128">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a6a8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a6a8-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a6a8-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a6a8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a6a8-130">See also</span></span>



[<span data-ttu-id="8a6a8-131">Outlook のアイテムとフィールド</span><span class="sxs-lookup"><span data-stu-id="8a6a8-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="8a6a8-132">新しいユーザー定義フィールドの定義を追加する</span><span class="sxs-lookup"><span data-stu-id="8a6a8-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="8a6a8-133">propertydefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="8a6a8-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="8a6a8-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8a6a8-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a6a8-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a6a8-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a6a8-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a6a8-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a6a8-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8a6a8-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

