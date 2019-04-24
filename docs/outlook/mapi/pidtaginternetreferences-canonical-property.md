---
title: PidTagInternetReferences 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360411"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="98aa4-103">PidTagInternetReferences 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98aa4-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="98aa4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98aa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98aa4-105">マルチパーパスインターネットメール内線 (MIME) メッセージの参照ヘッダーフィールドの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="98aa4-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98aa4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="98aa4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98aa4-107">PR_INTERNET_REFERENCES、PR_INTERNET_REFERENCES_A、PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="98aa4-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="98aa4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="98aa4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98aa4-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="98aa4-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="98aa4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="98aa4-110">Data type:</span></span>  <br/> |<span data-ttu-id="98aa4-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98aa4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="98aa4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="98aa4-112">Area:</span></span>  <br/> |<span data-ttu-id="98aa4-113">MIME</span><span class="sxs-lookup"><span data-stu-id="98aa4-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98aa4-114">解説</span><span class="sxs-lookup"><span data-stu-id="98aa4-114">Remarks</span></span>

<span data-ttu-id="98aa4-115">参照ヘッダーフィールドを生成するには、クライアントはこれらのプロパティを必要な値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98aa4-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="98aa4-116">MIME ライターは、これらのプロパティの値を References header フィールドにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98aa4-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="98aa4-117">これらのプロパティの値を設定するには、MIME クライアントは参照ヘッダーフィールドに必要な値を書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="98aa4-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="98aa4-118">MIME リーダーは、参照ヘッダーフィールドの値をこれらのプロパティにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98aa4-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="98aa4-119">MIME リーダーは、64 kb を超えた場合、これらのプロパティの値を切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="98aa4-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98aa4-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="98aa4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98aa4-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="98aa4-121">Protocol specifications</span></span>

<span data-ttu-id="98aa4-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98aa4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98aa4-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="98aa4-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98aa4-124">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98aa4-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98aa4-125">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="98aa4-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98aa4-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="98aa4-126">Header files</span></span>

<span data-ttu-id="98aa4-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98aa4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="98aa4-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="98aa4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="98aa4-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="98aa4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="98aa4-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98aa4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98aa4-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="98aa4-131">See also</span></span>



[<span data-ttu-id="98aa4-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="98aa4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98aa4-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98aa4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98aa4-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="98aa4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98aa4-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="98aa4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

