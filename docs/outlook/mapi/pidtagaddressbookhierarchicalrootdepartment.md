---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326125"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="1e6b3-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="1e6b3-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="1e6b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e6b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="1e6b3-105">階層アドレスルート (HAB) の識別名 (DN) を含みます。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e6b3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1e6b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e6b3-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT、PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="1e6b3-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="1e6b3-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="1e6b3-108">Property set:</span></span>  <br/> |<span data-ttu-id="1e6b3-109">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="1e6b3-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="1e6b3-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1e6b3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1e6b3-111">0x8c98</span><span class="sxs-lookup"><span data-stu-id="1e6b3-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="1e6b3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1e6b3-112">Data type:</span></span>  <br/> |<span data-ttu-id="1e6b3-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="1e6b3-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="1e6b3-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1e6b3-114">Area:</span></span>  <br/> |<span data-ttu-id="1e6b3-115">Exchange アドレス帳</span><span class="sxs-lookup"><span data-stu-id="1e6b3-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e6b3-116">解説</span><span class="sxs-lookup"><span data-stu-id="1e6b3-116">Remarks</span></span>

<span data-ttu-id="1e6b3-117">これはグローバルアドレス一覧 (GAL) コンテナーのプロパティであり、階層的なアドレスルートの識別名を表します。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="1e6b3-118">このプロパティは、オフラインアドレス帳にのみ存在し、Active Directory ドメインサービス (AD DS) には含まれません。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="1e6b3-119">呼び出し元は、リモートプロシージャコールを回避するために MAPI_CACHE_ONLY を GetProps 呼び出しに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="1e6b3-120">このパラメーターが存在しない場合、発信者は PT_OBJECT 型の PR_EMS_AB_HAB_ROOT_DEPARTMENT を使用して、ルート部署を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="1e6b3-121">ルート部門が取得されると、MAPI_MAILUSER または MAPI_DISTLIST のオブジェクトタイプを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="1e6b3-122">オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="1e6b3-123">オブジェクトの種類が MAPI_MAILUSER の場合、前のスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="1e6b3-124">Microsoft Office Outlook 2007 Service Pack 2 は、両方のスキーマをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="1e6b3-125">microsoft outlook 2010 および microsoft outlook 2013 は、新しいスキーマをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="1e6b3-126">新しいスキーマでは、すべての部署グループが配布リストであり、MAPI_DISTLIST 型でもあります。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="1e6b3-127">部署グループのメンバー、および部署グループ内の部署は、PR_EMS_AB_MEMBER を使用して配布リストのメンバーとまったく同じように取得されます。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="1e6b3-128">ルート部門が取得されると、MAPI_MAILUSER または MAPI_DISTLIST のオブジェクトタイプを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="1e6b3-129">オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="1e6b3-130">オブジェクトの種類が MAPI_MAILUSER の場合は、古いスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="1e6b3-131">新しいスキーマでは、すべての部署グループは dl でもあり、MAPI_DISTLIST 型です。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e6b3-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1e6b3-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e6b3-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1e6b3-133">Protocol specifications</span></span>

<span data-ttu-id="1e6b3-134">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e6b3-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e6b3-135">プロパティセットの定義と、関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e6b3-136">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1e6b3-136">Header files</span></span>

<span data-ttu-id="1e6b3-137">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e6b3-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e6b3-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e6b3-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e6b3-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e6b3-139">See also</span></span>



[<span data-ttu-id="1e6b3-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1e6b3-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e6b3-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e6b3-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e6b3-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1e6b3-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e6b3-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1e6b3-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

