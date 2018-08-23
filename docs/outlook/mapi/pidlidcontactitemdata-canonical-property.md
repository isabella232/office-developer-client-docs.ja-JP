---
title: PidLidContactItemData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f363b0a756a2cf4c7e37854cab0ddc4a46a0754d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582659"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="2c355-103">PidLidContactItemData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c355-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="2c355-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c355-105">連絡先情報を表示する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c355-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c355-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2c355-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c355-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="2c355-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="2c355-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2c355-108">Property set:</span></span>  <br/> |<span data-ttu-id="2c355-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="2c355-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="2c355-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2c355-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2c355-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="2c355-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="2c355-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2c355-112">Data type:</span></span>  <br/> |<span data-ttu-id="2c355-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2c355-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2c355-114">領域:</span><span class="sxs-lookup"><span data-stu-id="2c355-114">Area:</span></span>  <br/> |<span data-ttu-id="2c355-115">Contact</span><span class="sxs-lookup"><span data-stu-id="2c355-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c355-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2c355-116">Remarks</span></span>

<span data-ttu-id="2c355-117">存在する場合、プロパティには、各アプリケーションのユーザー インターフェイスに表示されるフィールドに対応する 6 つのエントリが必要です。</span><span class="sxs-lookup"><span data-stu-id="2c355-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="2c355-118">**複数値プロパティに 1 から始まるインデックス**</span><span class="sxs-lookup"><span data-stu-id="2c355-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="2c355-119">**値は、次のいずれかである必要があります。**</span><span class="sxs-lookup"><span data-stu-id="2c355-119">**The value must be one of the following**</span></span>|<span data-ttu-id="2c355-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="2c355-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c355-121">1</span><span class="sxs-lookup"><span data-stu-id="2c355-121">1</span></span>  <br/> |<span data-ttu-id="2c355-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c355-122">0x00000001</span></span>  <br/> |<span data-ttu-id="2c355-123">アプリケーションは、連絡先の自宅の住所を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c355-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="2c355-124">1</span><span class="sxs-lookup"><span data-stu-id="2c355-124">1</span></span>  <br/> |<span data-ttu-id="2c355-125">0x00000002、0x00000000 または</span><span class="sxs-lookup"><span data-stu-id="2c355-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="2c355-126">アプリケーションでは、取引先担当者の作業時間を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c355-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="2c355-127">1</span><span class="sxs-lookup"><span data-stu-id="2c355-127">1</span></span>  <br/> |<span data-ttu-id="2c355-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="2c355-128">0x00000003</span></span>  <br/> |<span data-ttu-id="2c355-129">アプリケーションを表示する必要があります、連絡先の他のアドレスです。</span><span class="sxs-lookup"><span data-stu-id="2c355-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="2c355-130">2</span><span class="sxs-lookup"><span data-stu-id="2c355-130">2</span></span>  <br/> |<span data-ttu-id="2c355-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="2c355-131">0x00008080</span></span>  <br/> |<span data-ttu-id="2c355-132">アプリケーションでは、Email1 を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c355-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="2c355-133">2</span><span class="sxs-lookup"><span data-stu-id="2c355-133">2</span></span>  <br/> |<span data-ttu-id="2c355-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="2c355-134">0x00008090</span></span>  <br/> |<span data-ttu-id="2c355-135">アプリケーションは、電子メール 2 を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c355-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="2c355-136">2</span><span class="sxs-lookup"><span data-stu-id="2c355-136">2</span></span>  <br/> |<span data-ttu-id="2c355-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="2c355-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="2c355-138">アプリケーションは、電子メール 3 を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c355-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="2c355-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="2c355-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="2c355-140">電話のプロパティのいずれかまたは[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている fax 番号のいずれかの PropertyID。</span><span class="sxs-lookup"><span data-stu-id="2c355-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="2c355-141">アプリケーションでは、対応するプロパティを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c355-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2c355-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2c355-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c355-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2c355-143">Protocol specifications</span></span>

<span data-ttu-id="2c355-144">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c355-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c355-145">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c355-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c355-146">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c355-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c355-147">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c355-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c355-148">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2c355-148">Header files</span></span>

<span data-ttu-id="2c355-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c355-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c355-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c355-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c355-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c355-151">See also</span></span>



[<span data-ttu-id="2c355-152">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c355-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c355-153">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c355-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c355-154">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2c355-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c355-155">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2c355-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

