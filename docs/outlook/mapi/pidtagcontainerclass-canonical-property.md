---
title: PidTagContainerClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283150"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="e3e98-103">PidTagContainerClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3e98-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="e3e98-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3e98-105">フォルダーの種類を説明するテキスト文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3e98-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="e3e98-106">このプロパティは一般に無視されます。Microsoft® Exchange Server 2003 メールボックス マネージャー Exchange Server前のバージョンでは、このプロパティが存在すると予想されます。</span><span class="sxs-lookup"><span data-stu-id="e3e98-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3e98-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e3e98-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3e98-108">PR_CONTAINER_CLASS、PR_CONTAINER_CLASS_A、PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="e3e98-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="e3e98-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="e3e98-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e3e98-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="e3e98-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="e3e98-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e3e98-111">Data type:</span></span>  <br/> |<span data-ttu-id="e3e98-112">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e3e98-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e3e98-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="e3e98-113">Area:</span></span>  <br/> |<span data-ttu-id="e3e98-114">Container</span><span class="sxs-lookup"><span data-stu-id="e3e98-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3e98-115">注釈</span><span class="sxs-lookup"><span data-stu-id="e3e98-115">Remarks</span></span>

<span data-ttu-id="e3e98-116">これらのプロパティは、通常、ユーザーが使用Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="e3e98-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="e3e98-117">ただし、Microsoft Office Outlook®フォルダーに添付します。</span><span class="sxs-lookup"><span data-stu-id="e3e98-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="e3e98-118">さらに、2003 メールボックス マネージャー Exchange Server以前Exchange Serverのバージョンでは、これらのプロパティを持つフォルダーが正しく処理されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e3e98-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="e3e98-119">これらのプロパティには、次の表の文字列値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e3e98-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="e3e98-120">**値**</span><span class="sxs-lookup"><span data-stu-id="e3e98-120">**Value**</span></span>|<span data-ttu-id="e3e98-121">**フォルダーの内容**</span><span class="sxs-lookup"><span data-stu-id="e3e98-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3e98-122">IPF.Appointment</span><span class="sxs-lookup"><span data-stu-id="e3e98-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="e3e98-123">予定</span><span class="sxs-lookup"><span data-stu-id="e3e98-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="e3e98-124">IPF.Contact</span><span class="sxs-lookup"><span data-stu-id="e3e98-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="e3e98-125">連絡先</span><span class="sxs-lookup"><span data-stu-id="e3e98-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="e3e98-126">IPF。ジャーナル</span><span class="sxs-lookup"><span data-stu-id="e3e98-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="e3e98-127">Outlookジャーナル エントリ</span><span class="sxs-lookup"><span data-stu-id="e3e98-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="e3e98-128">IPF.Note</span><span class="sxs-lookup"><span data-stu-id="e3e98-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="e3e98-129">メール メッセージとメモ</span><span class="sxs-lookup"><span data-stu-id="e3e98-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="e3e98-130">IPF。StickyNote</span><span class="sxs-lookup"><span data-stu-id="e3e98-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="e3e98-131">Outlook 付箋</span><span class="sxs-lookup"><span data-stu-id="e3e98-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="e3e98-132">IPF.Task</span><span class="sxs-lookup"><span data-stu-id="e3e98-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="e3e98-133">Outlook の仕事</span><span class="sxs-lookup"><span data-stu-id="e3e98-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="e3e98-134">メール メッセージを含むフォルダーの場合、これらのプロパティは IPF に設定する必要があります。注。</span><span class="sxs-lookup"><span data-stu-id="e3e98-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e3e98-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e3e98-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3e98-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e3e98-136">Protocol specifications</span></span>

<span data-ttu-id="e3e98-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3e98-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3e98-138">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e3e98-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3e98-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3e98-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3e98-140">メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3e98-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="e3e98-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3e98-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3e98-142">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3e98-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e3e98-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3e98-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3e98-144">連絡先および個人用配布リスト オブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3e98-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3e98-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e3e98-145">Header files</span></span>

<span data-ttu-id="e3e98-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3e98-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3e98-147">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3e98-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3e98-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e3e98-148">Mapitags.h</span></span>
  
> <span data-ttu-id="e3e98-149">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e3e98-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3e98-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3e98-150">See also</span></span>



[<span data-ttu-id="e3e98-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e3e98-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3e98-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3e98-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3e98-153">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e3e98-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3e98-154">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e3e98-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

