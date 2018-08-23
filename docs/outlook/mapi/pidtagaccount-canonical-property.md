---
title: PidTagAccount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab2efebe91f871452b243150367b83a1d53f8a52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802427"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="4fbfc-103">PidTagAccount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4fbfc-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="4fbfc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fbfc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fbfc-105">受信者のアカウント名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fbfc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4fbfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fbfc-107">PR_ACCOUNT、PR_ACCOUNT_A、PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="4fbfc-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="4fbfc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4fbfc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4fbfc-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="4fbfc-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="4fbfc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4fbfc-110">Data type:</span></span>  <br/> |<span data-ttu-id="4fbfc-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4fbfc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4fbfc-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4fbfc-112">Area:</span></span>  <br/> |<span data-ttu-id="4fbfc-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="4fbfc-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fbfc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4fbfc-114">Remarks</span></span>

<span data-ttu-id="4fbfc-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="4fbfc-116">受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="4fbfc-117">通常、これらのプロパティには、受信者の電子メール名、電子メール アドレスは、ローカル組織内の受信者を一意に識別するは、最終的なコンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="4fbfc-118">電子メール名は、短い形式の名前が特定のメッセージング ドメイン内で一意であることを保証するものでは X.400 の識別名に対応します。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4fbfc-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4fbfc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4fbfc-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4fbfc-120">Protocol specifications</span></span>

<span data-ttu-id="4fbfc-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fbfc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fbfc-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4fbfc-123">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fbfc-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fbfc-124">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="4fbfc-125">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fbfc-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fbfc-126">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4fbfc-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4fbfc-127">Header files</span></span>

<span data-ttu-id="4fbfc-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4fbfc-128">mapitags.h</span></span>
  
> <span data-ttu-id="4fbfc-129">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="4fbfc-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fbfc-130">mapidefs.h</span></span>
  
> <span data-ttu-id="4fbfc-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4fbfc-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fbfc-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fbfc-132">See also</span></span>



[<span data-ttu-id="4fbfc-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4fbfc-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="4fbfc-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4fbfc-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fbfc-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4fbfc-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fbfc-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4fbfc-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

