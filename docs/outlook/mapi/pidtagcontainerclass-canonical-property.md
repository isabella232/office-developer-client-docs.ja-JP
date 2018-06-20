---
title: PidTagContainerClass の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9d40c21cde6bf3a6e8e37dda80dd6f900f233a0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802590"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="243de-103">PidTagContainerClass の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="243de-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="243de-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="243de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="243de-105">フォルダーの種類を説明する文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="243de-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="243de-106">このプロパティを無視することが一般的には、Exchange Server 2003 のメールボックス マネージャーの前に、Microsoft® Exchange Server のバージョンはこのプロパティが存在することを期待しています。</span><span class="sxs-lookup"><span data-stu-id="243de-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="243de-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="243de-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="243de-108">PR_CONTAINER_CLASS、PR_CONTAINER_CLASS_A、PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="243de-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="243de-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="243de-109">Identifier:</span></span>  <br/> |<span data-ttu-id="243de-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="243de-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="243de-111">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="243de-111">Data type:</span></span>  <br/> |<span data-ttu-id="243de-112">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="243de-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="243de-113">領域:</span><span class="sxs-lookup"><span data-stu-id="243de-113">Area:</span></span>  <br/> |<span data-ttu-id="243de-114">Container</span><span class="sxs-lookup"><span data-stu-id="243de-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="243de-115">備考</span><span class="sxs-lookup"><span data-stu-id="243de-115">Remarks</span></span>

<span data-ttu-id="243de-116">これらのプロパティは、通常は Exchange Server では使用されません。</span><span class="sxs-lookup"><span data-stu-id="243de-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="243de-117">ただし、Microsoft Office Outlook® に添付のメールボックス フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="243de-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="243de-118">さらに、Exchange Server 2003 のメールボックス マネージャーの前に Exchange Server のバージョンが正しく処理されないこれらのプロパティを持たないフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="243de-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="243de-119">これらのプロパティは、次の表に文字列値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="243de-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="243de-120">**値**</span><span class="sxs-lookup"><span data-stu-id="243de-120">**Value**</span></span>|<span data-ttu-id="243de-121">**フォルダーの内容**</span><span class="sxs-lookup"><span data-stu-id="243de-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="243de-122">IPF.Appointment</span><span class="sxs-lookup"><span data-stu-id="243de-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="243de-123">予定</span><span class="sxs-lookup"><span data-stu-id="243de-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="243de-124">IPF.Contact</span><span class="sxs-lookup"><span data-stu-id="243de-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="243de-125">連絡先</span><span class="sxs-lookup"><span data-stu-id="243de-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="243de-126">IPF。仕訳帳</span><span class="sxs-lookup"><span data-stu-id="243de-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="243de-127">Outlook の仕訳帳のエントリ</span><span class="sxs-lookup"><span data-stu-id="243de-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="243de-128">IPF.Note</span><span class="sxs-lookup"><span data-stu-id="243de-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="243de-129">メール メッセージおよびノート</span><span class="sxs-lookup"><span data-stu-id="243de-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="243de-130">IPF。StickyNote</span><span class="sxs-lookup"><span data-stu-id="243de-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="243de-131">Outlook のメモ</span><span class="sxs-lookup"><span data-stu-id="243de-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="243de-132">IPF.Task</span><span class="sxs-lookup"><span data-stu-id="243de-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="243de-133">Outlook のタスク</span><span class="sxs-lookup"><span data-stu-id="243de-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="243de-134">メール メッセージが含まれるフォルダーでは、IPF にこれらのプロパティを設定する必要があります。注意してください。</span><span class="sxs-lookup"><span data-stu-id="243de-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="243de-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="243de-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="243de-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="243de-136">Protocol specifications</span></span>

<span data-ttu-id="243de-137">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="243de-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="243de-138">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="243de-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="243de-139">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="243de-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="243de-140">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="243de-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="243de-141">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="243de-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="243de-142">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="243de-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="243de-143">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="243de-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="243de-144">プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="243de-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="243de-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="243de-145">Header files</span></span>

<span data-ttu-id="243de-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="243de-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="243de-147">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="243de-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="243de-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="243de-148">Mapitags.h</span></span>
  
> <span data-ttu-id="243de-149">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="243de-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="243de-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="243de-150">See also</span></span>



[<span data-ttu-id="243de-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="243de-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="243de-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="243de-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="243de-153">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="243de-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="243de-154">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="243de-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

