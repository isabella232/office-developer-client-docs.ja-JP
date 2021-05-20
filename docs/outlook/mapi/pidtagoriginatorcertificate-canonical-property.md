---
title: PidTagOriginatorCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d367073de2134ff766cbae3d4f6bcfa30b862122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438940"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="f2017-103">PidTagOriginatorCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2017-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="f2017-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2017-105">メッセージ発信元の ASN.1 証明書が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f2017-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2017-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f2017-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2017-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="f2017-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="f2017-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f2017-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2017-109">0x0022</span><span class="sxs-lookup"><span data-stu-id="f2017-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="f2017-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f2017-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2017-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f2017-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f2017-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f2017-112">Area:</span></span>  <br/> |<span data-ttu-id="f2017-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f2017-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2017-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f2017-114">Remarks</span></span>

<span data-ttu-id="f2017-115">このプロパティは、発信者のプロパティ ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md) **)** プロパティPR_USER_CERTIFICATEコピーです。</span><span class="sxs-lookup"><span data-stu-id="f2017-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2017-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f2017-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f2017-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f2017-117">Header files</span></span>

<span data-ttu-id="f2017-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2017-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2017-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2017-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2017-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2017-120">Mapitags.h</span></span>
  
> <span data-ttu-id="f2017-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f2017-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2017-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2017-122">See also</span></span>



[<span data-ttu-id="f2017-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f2017-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2017-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2017-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2017-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f2017-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2017-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f2017-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

