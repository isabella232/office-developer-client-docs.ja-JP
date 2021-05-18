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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326125"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="adac4-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="adac4-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="adac4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adac4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="adac4-105">階層アドレス ルート (HAB) の識別名 (DN) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="adac4-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="adac4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="adac4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="adac4-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT,PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="adac4-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="adac4-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="adac4-108">Property set:</span></span>  <br/> |<span data-ttu-id="adac4-109">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="adac4-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="adac4-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="adac4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="adac4-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="adac4-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="adac4-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="adac4-112">Data type:</span></span>  <br/> |<span data-ttu-id="adac4-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="adac4-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="adac4-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="adac4-114">Area:</span></span>  <br/> |<span data-ttu-id="adac4-115">Exchangeアドレス帳</span><span class="sxs-lookup"><span data-stu-id="adac4-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adac4-116">注釈</span><span class="sxs-lookup"><span data-stu-id="adac4-116">Remarks</span></span>

<span data-ttu-id="adac4-117">これはグローバル アドレス一覧 (GAL) コンテナーのプロパティであり、階層型アドレス ルートの識別名を表します。</span><span class="sxs-lookup"><span data-stu-id="adac4-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="adac4-118">このプロパティはオフライン アドレス帳にのみ存在し、Active Directory ドメイン サービス (DS) にはADされません。</span><span class="sxs-lookup"><span data-stu-id="adac4-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="adac4-119">呼び出し元は、MAPI_CACHE_ONLYプロシージャ呼び出しを回避するために、GetProps 呼び出しに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="adac4-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="adac4-120">これが存在しない場合、発信者はルート部門PR_EMS_AB_HAB_ROOT_DEPARTMENTの種類である PT_OBJECT を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adac4-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="adac4-121">ルート部門を取得すると、オブジェクトの種類を指定MAPI_MAILUSERまたはMAPI_DISTLIST。</span><span class="sxs-lookup"><span data-stu-id="adac4-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="adac4-122">オブジェクトの種類が変更MAPI_DISTLIST新しいスキーマが採用されています。</span><span class="sxs-lookup"><span data-stu-id="adac4-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="adac4-123">オブジェクトの種類が変更MAPI_MAILUSER前のスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="adac4-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="adac4-124">Microsoft Office Outlook 2007 Service Pack 2 では、両方のスキーマがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="adac4-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="adac4-125">Microsoft Outlook 2010とMicrosoft Outlook 2013スキーマをサポートします。</span><span class="sxs-lookup"><span data-stu-id="adac4-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="adac4-126">新しいスキーマでは、すべての部門グループも配布リストであり、種類は MAPI_DISTLIST。</span><span class="sxs-lookup"><span data-stu-id="adac4-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="adac4-127">部署グループのメンバー、および部門グループ内の部署は、配布リスト のメンバーとまったく同PR_EMS_AB_MEMBERを使用して取得されます。</span><span class="sxs-lookup"><span data-stu-id="adac4-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="adac4-128">ルート部門を取得すると、オブジェクトの種類を指定MAPI_MAILUSERまたはMAPI_DISTLIST。</span><span class="sxs-lookup"><span data-stu-id="adac4-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="adac4-129">オブジェクトの種類が指定されているMAPI_DISTLIST、新しいスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="adac4-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="adac4-130">オブジェクトの種類が指定されているMAPI_MAILUSER、古いスキーマが使用されています。</span><span class="sxs-lookup"><span data-stu-id="adac4-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="adac4-131">新しいスキーマでは、すべての部署グループも LS で、グループの種類MAPI_DISTLIST。</span><span class="sxs-lookup"><span data-stu-id="adac4-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="adac4-132">関連リソース</span><span class="sxs-lookup"><span data-stu-id="adac4-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="adac4-133">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="adac4-133">Protocol specifications</span></span>

<span data-ttu-id="adac4-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adac4-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adac4-135">プロパティ セットの定義と、関連するプロトコル仕様へのMicrosoft Exchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="adac4-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="adac4-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="adac4-136">Header files</span></span>

<span data-ttu-id="adac4-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adac4-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="adac4-138">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="adac4-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adac4-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="adac4-139">See also</span></span>



[<span data-ttu-id="adac4-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="adac4-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="adac4-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="adac4-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="adac4-142">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="adac4-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="adac4-143">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="adac4-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

