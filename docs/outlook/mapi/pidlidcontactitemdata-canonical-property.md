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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319511"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="bb76a-103">PidLidContactItemData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb76a-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="bb76a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb76a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb76a-105">連絡先情報を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb76a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bb76a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb76a-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="bb76a-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="bb76a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="bb76a-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb76a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="bb76a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="bb76a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bb76a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bb76a-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="bb76a-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="bb76a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bb76a-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb76a-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="bb76a-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="bb76a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bb76a-114">Area:</span></span>  <br/> |<span data-ttu-id="bb76a-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="bb76a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb76a-116">解説</span><span class="sxs-lookup"><span data-stu-id="bb76a-116">Remarks</span></span>

<span data-ttu-id="bb76a-117">指定する場合、プロパティには、アプリケーションのユーザーインターフェイスで表示されるフィールドに対応する6つのエントリが必要です。</span><span class="sxs-lookup"><span data-stu-id="bb76a-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="bb76a-118">**複数値を持つプロパティへの1から始まるインデックス**</span><span class="sxs-lookup"><span data-stu-id="bb76a-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="bb76a-119">**この値は、次のいずれかであることが必要です。**</span><span class="sxs-lookup"><span data-stu-id="bb76a-119">**The value must be one of the following**</span></span>|<span data-ttu-id="bb76a-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="bb76a-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb76a-121">1-d</span><span class="sxs-lookup"><span data-stu-id="bb76a-121">1</span></span>  <br/> |<span data-ttu-id="bb76a-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bb76a-122">0x00000001</span></span>  <br/> |<span data-ttu-id="bb76a-123">アプリケーションには、連絡先の自宅の住所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="bb76a-124">1-d</span><span class="sxs-lookup"><span data-stu-id="bb76a-124">1</span></span>  <br/> |<span data-ttu-id="bb76a-125">0x00000002 または0x00000000</span><span class="sxs-lookup"><span data-stu-id="bb76a-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="bb76a-126">アプリケーションに連絡先の仕事が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="bb76a-127">1-d</span><span class="sxs-lookup"><span data-stu-id="bb76a-127">1</span></span>  <br/> |<span data-ttu-id="bb76a-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="bb76a-128">0x00000003</span></span>  <br/> |<span data-ttu-id="bb76a-129">アプリケーションには、連絡先のその他のアドレスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="bb76a-130">pbm-2</span><span class="sxs-lookup"><span data-stu-id="bb76a-130">2</span></span>  <br/> |<span data-ttu-id="bb76a-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="bb76a-131">0x00008080</span></span>  <br/> |<span data-ttu-id="bb76a-132">アプリケーションに Email1 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="bb76a-133">pbm-2</span><span class="sxs-lookup"><span data-stu-id="bb76a-133">2</span></span>  <br/> |<span data-ttu-id="bb76a-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="bb76a-134">0x00008090</span></span>  <br/> |<span data-ttu-id="bb76a-135">アプリケーションに Email2 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="bb76a-136">pbm-2</span><span class="sxs-lookup"><span data-stu-id="bb76a-136">2</span></span>  <br/> |<span data-ttu-id="bb76a-137">0x000080a0</span><span class="sxs-lookup"><span data-stu-id="bb76a-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="bb76a-138">アプリケーションに Email3 が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="bb76a-139">3、4、5、6</span><span class="sxs-lookup"><span data-stu-id="bb76a-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="bb76a-140">PropertyID [[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている電話のプロパティまたは fax 番号のいずれかを指定します。</span><span class="sxs-lookup"><span data-stu-id="bb76a-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="bb76a-141">アプリケーションには、対応するプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb76a-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bb76a-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb76a-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb76a-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bb76a-143">Protocol specifications</span></span>

<span data-ttu-id="bb76a-144">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb76a-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb76a-145">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb76a-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb76a-146">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb76a-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb76a-147">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb76a-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb76a-148">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bb76a-148">Header files</span></span>

<span data-ttu-id="bb76a-149">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb76a-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb76a-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb76a-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb76a-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb76a-151">See also</span></span>



[<span data-ttu-id="bb76a-152">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bb76a-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb76a-153">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb76a-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb76a-154">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb76a-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb76a-155">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb76a-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

