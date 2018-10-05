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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400258"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="47242-103">PidTagContainerClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47242-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="47242-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47242-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47242-105">フォルダーの種類を説明する文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47242-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="47242-106">このプロパティを無視することが一般的には、Exchange Server 2003 のメールボックス マネージャーの前に、Microsoft® Exchange Server のバージョンはこのプロパティが存在することを期待しています。</span><span class="sxs-lookup"><span data-stu-id="47242-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47242-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47242-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="47242-108">PR_CONTAINER_CLASS、PR_CONTAINER_CLASS_A、PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="47242-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="47242-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="47242-109">Identifier:</span></span>  <br/> |<span data-ttu-id="47242-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="47242-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="47242-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47242-111">Data type:</span></span>  <br/> |<span data-ttu-id="47242-112">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47242-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="47242-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="47242-113">Area:</span></span>  <br/> |<span data-ttu-id="47242-114">Container</span><span class="sxs-lookup"><span data-stu-id="47242-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47242-115">備考</span><span class="sxs-lookup"><span data-stu-id="47242-115">Remarks</span></span>

<span data-ttu-id="47242-116">これらのプロパティは、通常は Exchange Server では使用されません。</span><span class="sxs-lookup"><span data-stu-id="47242-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="47242-117">ただし、Microsoft Office Outlook® に添付のメールボックス フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="47242-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="47242-118">さらに、Exchange Server 2003 のメールボックス マネージャーの前に Exchange Server のバージョンが正しく処理されないこれらのプロパティを持たないフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="47242-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="47242-119">これらのプロパティは、次の表に文字列値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="47242-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="47242-120">**値**</span><span class="sxs-lookup"><span data-stu-id="47242-120">**Value**</span></span>|<span data-ttu-id="47242-121">**フォルダーの内容**</span><span class="sxs-lookup"><span data-stu-id="47242-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47242-122">IPF.Appointment</span><span class="sxs-lookup"><span data-stu-id="47242-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="47242-123">予定</span><span class="sxs-lookup"><span data-stu-id="47242-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="47242-124">IPF.Contact</span><span class="sxs-lookup"><span data-stu-id="47242-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="47242-125">連絡先</span><span class="sxs-lookup"><span data-stu-id="47242-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="47242-126">IPF。仕訳帳</span><span class="sxs-lookup"><span data-stu-id="47242-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="47242-127">Outlook の仕訳帳のエントリ</span><span class="sxs-lookup"><span data-stu-id="47242-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="47242-128">IPF.Note</span><span class="sxs-lookup"><span data-stu-id="47242-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="47242-129">メール メッセージおよびノート</span><span class="sxs-lookup"><span data-stu-id="47242-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="47242-130">IPF。StickyNote</span><span class="sxs-lookup"><span data-stu-id="47242-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="47242-131">Outlook のメモ</span><span class="sxs-lookup"><span data-stu-id="47242-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="47242-132">IPF.Task</span><span class="sxs-lookup"><span data-stu-id="47242-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="47242-133">Outlook のタスク</span><span class="sxs-lookup"><span data-stu-id="47242-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="47242-134">メール メッセージが含まれるフォルダーでは、IPF にこれらのプロパティを設定する必要があります。注意してください。</span><span class="sxs-lookup"><span data-stu-id="47242-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47242-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47242-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47242-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47242-136">Protocol specifications</span></span>

<span data-ttu-id="47242-137">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47242-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47242-138">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="47242-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47242-139">[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47242-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47242-140">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47242-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="47242-141">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47242-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47242-142">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47242-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="47242-143">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47242-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47242-144">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47242-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47242-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="47242-145">Header files</span></span>

<span data-ttu-id="47242-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47242-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="47242-147">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47242-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="47242-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47242-148">Mapitags.h</span></span>
  
> <span data-ttu-id="47242-149">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47242-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47242-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="47242-150">See also</span></span>



[<span data-ttu-id="47242-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47242-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47242-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47242-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47242-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47242-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47242-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47242-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

