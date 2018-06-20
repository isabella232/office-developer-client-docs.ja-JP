---
title: PidTagUserFields の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803653"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="5a485-103">PidTagUserFields の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5a485-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="5a485-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a485-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a485-105">名前、データ型、およびその他のユーザー定義のフィールド情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a485-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a485-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5a485-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a485-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="5a485-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="5a485-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5a485-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a485-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="5a485-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="5a485-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5a485-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a485-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a485-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a485-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5a485-112">Area:</span></span>  <br/> |<span data-ttu-id="5a485-113">MAPI フォルダー</span><span class="sxs-lookup"><span data-stu-id="5a485-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a485-114">備考</span><span class="sxs-lookup"><span data-stu-id="5a485-114">Remarks</span></span>

<span data-ttu-id="5a485-115">、各項目については、Outlook は、対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティにユーザー定義のすべてのフィールドの定義を格納します。</span><span class="sxs-lookup"><span data-stu-id="5a485-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="5a485-116">**PidLidPropertyDefinitionStream**プロパティには、 [PropertyDefinition](propertydefinition-stream-structure.md)、フィールド定義が含まれていると呼ばれるバイナリ ストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a485-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="5a485-117">ストリームの構造体フィールドの定義の詳細については、[ストリームの構造](stream-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a485-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="5a485-118">フォルダーごとには、Outlook は、関連付けられたメッセージのメッセージ クラスの IPC.MS の**PidTagUserFields**プロパティには、そのフォルダー内のすべてのユーザー定義フィールドの定義を格納します。REN。USERFIELDS の各フォルダーはその内容が関連付けられているテーブルでは、このクラスの複数のメッセージが含まれていると推定します。</span><span class="sxs-lookup"><span data-stu-id="5a485-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5a485-119">フォルダー内のユーザー定義フィールドのセットは可能性があります必ずしもその項目の各フィールドのユーザー定義の設定を一致しません。</span><span class="sxs-lookup"><span data-stu-id="5a485-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="5a485-120">一連のフォルダー内のユーザー定義フィールドは、フォルダーの [フィールドの選択など、Outlook の UI でのさまざまな場所に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a485-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="5a485-121">メッセージの**PidTagUserFields**プロパティには、バイナリ ストリーム、 **FolderUserFields**、フォルダー フィールドの定義が含まれているが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a485-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="5a485-122">フォルダー フィールドの定義については、ストリームの構造体の詳細については、[フォルダー フィールドのストリームの構造体](folder-fields-stream-structures.md)および[FolderUserFields ストリームのサンプル](folderuserfields-stream-sample.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a485-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="5a485-123">セクションの見出し</span><span class="sxs-lookup"><span data-stu-id="5a485-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a485-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5a485-124">Protocol specifications</span></span>

<span data-ttu-id="5a485-125">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a485-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a485-126">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a485-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a485-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5a485-127">Header files</span></span>

<span data-ttu-id="5a485-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a485-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a485-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a485-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a485-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a485-130">See also</span></span>



[<span data-ttu-id="5a485-131">Outlook アイテムおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="5a485-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="5a485-132">新しいユーザー定義フィールドの定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="5a485-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="5a485-133">PropertyDefinition ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="5a485-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="5a485-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a485-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a485-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a485-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a485-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5a485-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a485-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5a485-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

