---
title: PidLidCustomFlag の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5d97f56946512266bb7a08aa6b4a4ff78dded56a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801868"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="90ede-103">PidLidCustomFlag の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="90ede-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="90ede-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90ede-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90ede-105">指定するビットマスク メッセージは、カスタマイズ方法、たとえば、カスタム プロパティを保存します。</span><span class="sxs-lookup"><span data-stu-id="90ede-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="90ede-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="90ede-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90ede-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="90ede-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="90ede-108">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="90ede-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="90ede-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="90ede-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="90ede-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="90ede-110">Data type:</span></span>  <br/> |<span data-ttu-id="90ede-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90ede-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90ede-112">備考</span><span class="sxs-lookup"><span data-stu-id="90ede-112">Remarks</span></span>

<span data-ttu-id="90ede-113">このプロパティの値を取得するには、まず**[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** を使用して、プロパティ タグを取得して値を取得する**[IMAPIProp::GetProps](imapiprop-getprops.md)** でこのプロパティのタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="90ede-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="90ede-114">使用できるフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="90ede-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="90ede-115">**定数**</span><span class="sxs-lookup"><span data-stu-id="90ede-115">**Constant**</span></span>|<span data-ttu-id="90ede-116">**値**</span><span class="sxs-lookup"><span data-stu-id="90ede-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90ede-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="90ede-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="90ede-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="90ede-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="90ede-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="90ede-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="90ede-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="90ede-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="90ede-121">**IMAPIProp::GetIDsFromNames**を呼び出すときは、 *lppPropNames*の入力パラメーターで指定された**[MAPINAMEID](mapinameid.md)** 構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="90ede-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="90ede-122">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="90ede-122">**Member**</span></span>|<span data-ttu-id="90ede-123">**値**</span><span class="sxs-lookup"><span data-stu-id="90ede-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90ede-124">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="90ede-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="90ede-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="90ede-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="90ede-126">ulKind。</span><span class="sxs-lookup"><span data-stu-id="90ede-126">ulKind:</span></span>  <br/> |<span data-ttu-id="90ede-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="90ede-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="90ede-128">Kind.lID。</span><span class="sxs-lookup"><span data-stu-id="90ede-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="90ede-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="90ede-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="90ede-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="90ede-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90ede-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="90ede-131">Protocol specifications</span></span>

<span data-ttu-id="90ede-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90ede-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90ede-133">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90ede-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90ede-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="90ede-134">Header files</span></span>

<span data-ttu-id="90ede-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90ede-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="90ede-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90ede-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="90ede-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90ede-137">Mapitags.h</span></span>
  
> <span data-ttu-id="90ede-138">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="90ede-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90ede-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="90ede-139">See also</span></span>



[<span data-ttu-id="90ede-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="90ede-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90ede-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="90ede-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90ede-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="90ede-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90ede-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="90ede-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

