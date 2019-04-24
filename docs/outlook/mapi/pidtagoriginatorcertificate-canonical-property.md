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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d367073de2134ff766cbae3d4f6bcfa30b862122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351108"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="1f586-103">PidTagOriginatorCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f586-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="1f586-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f586-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f586-105">メッセージ発信者の ASN. 1 証明書が保存されています。</span><span class="sxs-lookup"><span data-stu-id="1f586-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f586-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1f586-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f586-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="1f586-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="1f586-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1f586-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f586-109">0x0022</span><span class="sxs-lookup"><span data-stu-id="1f586-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="1f586-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1f586-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f586-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1f586-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1f586-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1f586-112">Area:</span></span>  <br/> |<span data-ttu-id="1f586-113">MIME</span><span class="sxs-lookup"><span data-stu-id="1f586-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f586-114">解説</span><span class="sxs-lookup"><span data-stu-id="1f586-114">Remarks</span></span>

<span data-ttu-id="1f586-115">このプロパティは、オリジネータの**PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) プロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="1f586-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1f586-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1f586-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1f586-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1f586-117">Header files</span></span>

<span data-ttu-id="1f586-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f586-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f586-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f586-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f586-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1f586-120">Mapitags.h</span></span>
  
> <span data-ttu-id="1f586-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1f586-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f586-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f586-122">See also</span></span>



[<span data-ttu-id="1f586-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1f586-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f586-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f586-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f586-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1f586-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f586-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1f586-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

