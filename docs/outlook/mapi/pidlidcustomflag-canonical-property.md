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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357618"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="9d7df-103">PidLidCustomFlag 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d7df-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="9d7df-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d7df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d7df-105">メッセージをカスタマイズする方法を指定するビットマスク。たとえば、カスタムプロパティと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="9d7df-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="9d7df-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9d7df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d7df-107">dispidcustomflag</span><span class="sxs-lookup"><span data-stu-id="9d7df-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="9d7df-108">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9d7df-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9d7df-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="9d7df-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="9d7df-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9d7df-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d7df-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9d7df-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d7df-112">解説</span><span class="sxs-lookup"><span data-stu-id="9d7df-112">Remarks</span></span>

<span data-ttu-id="9d7df-113">このプロパティの値を取得するには、最初に**[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)** を使用してプロパティタグを取得し、次に**[imapiprop:: GetProps](imapiprop-getprops.md)** でこのプロパティタグを指定して、値を取得します。</span><span class="sxs-lookup"><span data-stu-id="9d7df-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="9d7df-114">可能なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d7df-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="9d7df-115">**定数**</span><span class="sxs-lookup"><span data-stu-id="9d7df-115">**Constant**</span></span>|<span data-ttu-id="9d7df-116">**値**</span><span class="sxs-lookup"><span data-stu-id="9d7df-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d7df-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="9d7df-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="9d7df-118">0x0d000000</span><span class="sxs-lookup"><span data-stu-id="9d7df-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="9d7df-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="9d7df-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="9d7df-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="9d7df-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="9d7df-121">**imapiprop:: getidsfromnames**を呼び出す場合は、入力パラメーター *lpppropnames*で示される**[mapinameid](mapinameid.md)** 構造体に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d7df-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="9d7df-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="9d7df-122">**Member**</span></span>|<span data-ttu-id="9d7df-123">**値**</span><span class="sxs-lookup"><span data-stu-id="9d7df-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d7df-124">lpguid:</span><span class="sxs-lookup"><span data-stu-id="9d7df-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="9d7df-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9d7df-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9d7df-126">ulkind:</span><span class="sxs-lookup"><span data-stu-id="9d7df-126">ulKind:</span></span>  <br/> |<span data-ttu-id="9d7df-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="9d7df-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="9d7df-128">ふたの種類:</span><span class="sxs-lookup"><span data-stu-id="9d7df-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="9d7df-129">dispidcustomflag</span><span class="sxs-lookup"><span data-stu-id="9d7df-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9d7df-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9d7df-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d7df-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9d7df-131">Protocol specifications</span></span>

<span data-ttu-id="9d7df-132">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d7df-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d7df-133">プロパティセットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d7df-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d7df-134">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9d7df-134">Header files</span></span>

<span data-ttu-id="9d7df-135">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d7df-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d7df-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d7df-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d7df-137">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9d7df-137">Mapitags.h</span></span>
  
> <span data-ttu-id="9d7df-138">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9d7df-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d7df-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="9d7df-139">See also</span></span>



[<span data-ttu-id="9d7df-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9d7df-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d7df-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9d7df-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d7df-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d7df-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d7df-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9d7df-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

