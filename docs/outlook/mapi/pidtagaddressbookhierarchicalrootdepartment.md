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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382611"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="677b8-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="677b8-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="677b8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="677b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="677b8-105">(HAB) の階層構造のアドレスのルートの識別名 (DN) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="677b8-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="677b8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="677b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="677b8-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT、PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="677b8-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="677b8-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="677b8-108">Property set:</span></span>  <br/> |<span data-ttu-id="677b8-109">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="677b8-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="677b8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="677b8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="677b8-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="677b8-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="677b8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="677b8-112">Data type:</span></span>  <br/> |<span data-ttu-id="677b8-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="677b8-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="677b8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="677b8-114">Area:</span></span>  <br/> |<span data-ttu-id="677b8-115">Exchange アドレス帳</span><span class="sxs-lookup"><span data-stu-id="677b8-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="677b8-116">備考</span><span class="sxs-lookup"><span data-stu-id="677b8-116">Remarks</span></span>

<span data-ttu-id="677b8-117">これは、グローバル アドレス一覧 (GAL) コンテナーのプロパティであり、階層的なアドレスのルートの識別名を表します。</span><span class="sxs-lookup"><span data-stu-id="677b8-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="677b8-118">このプロパティは、Active Directory ドメイン サービス (AD DS) しないとオフライン アドレス帳に存在だけです。</span><span class="sxs-lookup"><span data-stu-id="677b8-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="677b8-119">呼び出し元は、リモート プロシージャ呼び出しを避けるために GetProps 呼び出しに MAPI_CACHE_ONLY を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="677b8-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="677b8-120">これが存在しない場合、呼び出し元は、ルート部署が見つかりません PT_OBJECT の種類は、PR_EMS_AB_HAB_ROOT_DEPARTMENT を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="677b8-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="677b8-121">ルート部署が取得した後は、MAPI_MAILUSER または MAPI_DISTLIST オブジェクトの種類があります。</span><span class="sxs-lookup"><span data-stu-id="677b8-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="677b8-122">オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマを採用します。</span><span class="sxs-lookup"><span data-stu-id="677b8-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="677b8-123">オブジェクトの種類が MAPI_MAILUSER の場合は、前のスキーマを採用されています。</span><span class="sxs-lookup"><span data-stu-id="677b8-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="677b8-124">Microsoft Office Outlook 2007 Service Pack 2 には、両方のスキーマがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="677b8-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="677b8-125">Microsoft Outlook 2010 および Microsoft Outlook 2013 は、新しいスキーマをサポートします。</span><span class="sxs-lookup"><span data-stu-id="677b8-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="677b8-126">新しいスキーマで部門のすべてのグループも、配布リスト、MAPI_DISTLIST の種類の。</span><span class="sxs-lookup"><span data-stu-id="677b8-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="677b8-127">部門のグループ、および部門別のグループ内の部門のメンバーを取得するには、配布リストのメンバーと同様に PR_EMS_AB_MEMBER を使用します。</span><span class="sxs-lookup"><span data-stu-id="677b8-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="677b8-128">ルート部署が取得した後は、MAPI_MAILUSER または MAPI_DISTLIST オブジェクトの種類があります。</span><span class="sxs-lookup"><span data-stu-id="677b8-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="677b8-129">オブジェクトの種類が MAPI_DISTLIST の場合は、新しいスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="677b8-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="677b8-130">オブジェクトの種類が MAPI_MAILUSER の場合は、古いスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="677b8-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="677b8-131">新しいスキーマですべての部門別のグループも Dl、型 MAPI_DISTLIST の。</span><span class="sxs-lookup"><span data-stu-id="677b8-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="677b8-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="677b8-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="677b8-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="677b8-133">Protocol specifications</span></span>

<span data-ttu-id="677b8-134">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="677b8-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="677b8-135">プロパティ セットの定義と関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="677b8-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="677b8-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="677b8-136">Header files</span></span>

<span data-ttu-id="677b8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="677b8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="677b8-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="677b8-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="677b8-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="677b8-139">See also</span></span>



[<span data-ttu-id="677b8-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="677b8-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="677b8-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="677b8-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="677b8-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="677b8-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="677b8-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="677b8-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

