---
title: PidLidCustomFlag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384200"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="e5cd6-103">PidLidCustomFlag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5cd6-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="e5cd6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5cd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5cd6-105">指定するビットマスク メッセージは、カスタマイズ方法、たとえば、カスタム プロパティを保存します。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="e5cd6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e5cd6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5cd6-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="e5cd6-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="e5cd6-108">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e5cd6-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e5cd6-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="e5cd6-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="e5cd6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e5cd6-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5cd6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e5cd6-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5cd6-112">備考</span><span class="sxs-lookup"><span data-stu-id="e5cd6-112">Remarks</span></span>

<span data-ttu-id="e5cd6-113">このプロパティの値を取得するには、まず**[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** を使用して、プロパティ タグを取得して値を取得する**[IMAPIProp::GetProps](imapiprop-getprops.md)** でこのプロパティのタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="e5cd6-114">使用できるフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="e5cd6-115">**定数**</span><span class="sxs-lookup"><span data-stu-id="e5cd6-115">**Constant**</span></span>|<span data-ttu-id="e5cd6-116">**値**</span><span class="sxs-lookup"><span data-stu-id="e5cd6-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5cd6-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="e5cd6-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="e5cd6-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="e5cd6-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="e5cd6-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="e5cd6-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="e5cd6-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="e5cd6-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="e5cd6-121">**IMAPIProp::GetIDsFromNames**を呼び出すときは、 *lppPropNames*の入力パラメーターで指定された**[MAPINAMEID](mapinameid.md)** 構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="e5cd6-122">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="e5cd6-122">**Member**</span></span>|<span data-ttu-id="e5cd6-123">**値**</span><span class="sxs-lookup"><span data-stu-id="e5cd6-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5cd6-124">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="e5cd6-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e5cd6-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e5cd6-126">ulKind。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-126">ulKind:</span></span>  <br/> |<span data-ttu-id="e5cd6-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="e5cd6-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="e5cd6-128">Kind.lID。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="e5cd6-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="e5cd6-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e5cd6-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e5cd6-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5cd6-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e5cd6-131">Protocol specifications</span></span>

<span data-ttu-id="e5cd6-132">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5cd6-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5cd6-133">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5cd6-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e5cd6-134">Header files</span></span>

<span data-ttu-id="e5cd6-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5cd6-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5cd6-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5cd6-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5cd6-137">Mapitags.h</span></span>
  
> <span data-ttu-id="e5cd6-138">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5cd6-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5cd6-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5cd6-139">See also</span></span>



[<span data-ttu-id="e5cd6-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5cd6-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5cd6-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5cd6-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5cd6-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5cd6-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5cd6-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5cd6-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

