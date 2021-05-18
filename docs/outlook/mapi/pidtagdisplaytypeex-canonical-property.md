---
title: PidTagDisplayTypeEx 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360775"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="b56c0-103">PidTagDisplayTypeEx 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56c0-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="b56c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b56c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b56c0-105">グローバル アドレス一覧のテーブル内の行にエントリを表示する方法に関して、エントリの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b56c0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b56c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b56c0-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="b56c0-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="b56c0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b56c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b56c0-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="b56c0-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="b56c0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b56c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b56c0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b56c0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b56c0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b56c0-112">Area:</span></span>  <br/> |<span data-ttu-id="b56c0-113">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="b56c0-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b56c0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b56c0-114">Remarks</span></span>

<span data-ttu-id="b56c0-115">このプロパティは、グローバル アドレス一覧での表示方法に関して、エントリの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="b56c0-116">この情報は、このプロパティ [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)**で** PR_DISPLAY_TYPE追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b56c0-117">プロパティとこのプロパティ **のPR_DISPLAY_TYPE** は "DT_" で始まり、Mapitags.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="b56c0-118">文書化されていないすべての値は、MAPI 用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="b56c0-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="b56c0-119">クライアント アプリケーションは、新しい値を定義し、文書化されていない値を処理する準備をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b56c0-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="b56c0-120">ローカル、リモート、セキュリティ制御など、オブジェクトの属性を特定するのに役立つマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="b56c0-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="b56c0-121">これらのマクロには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-121">These macros include:</span></span> 
  
|<span data-ttu-id="b56c0-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="b56c0-122">**Macro**</span></span>|<span data-ttu-id="b56c0-123">**値**</span><span class="sxs-lookup"><span data-stu-id="b56c0-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b56c0-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="b56c0-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="b56c0-125">0x80000000)</span><span class="sxs-lookup"><span data-stu-id="b56c0-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="b56c0-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="b56c0-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="b56c0-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="b56c0-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="b56c0-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="b56c0-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="b56c0-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="b56c0-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="b56c0-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="b56c0-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="b56c0-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="b56c0-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="b56c0-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="b56c0-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="b56c0-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="b56c0-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="b56c0-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="b56c0-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="b56c0-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="b56c0-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="b56c0-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="b56c0-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="b56c0-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="b56c0-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="b56c0-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="b56c0-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="b56c0-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="b56c0-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="b56c0-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="b56c0-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="b56c0-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="b56c0-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="b56c0-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="b56c0-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="b56c0-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="b56c0-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="b56c0-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b56c0-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b56c0-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="b56c0-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="b56c0-146">これらのマクロの使い方に関する注意事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="b56c0-147">エントリが別のフォレストのリモート エントリであるかどうかを確認するには、DTE_IS_REMOTE_VALID マクロをこのプロパティの値に適用して、DTE_FLAG_REMOTE_VALID フラグがエントリに設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="b56c0-148">リモート エントリの場合は、リモート エントリの種類を確認するには、次のマクロを使用DTE_REMOTEできます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="b56c0-149">単一フォレスト構成とフォレスト間構成の両方で **、PR_DISPLAY_TYPE** の値が DT_DISTLIST で、DTE_IS_REMOTE_VALID が false の場合、マクロ DTE_LOCAL をこのプロパティの値に適用すると、オブジェクトの種類をさらに DT_DISTLIST (配布リスト) または DT_SEC_DISTLIST (セキュリティ配布リスト) として識別できます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="b56c0-150">マクロ を DTE_LOCAL の値に適用PR_DISPLAY_TYPE_EX型をDT_REMOTE_MAILUSERすると、エントリはリモート エントリになります。</span><span class="sxs-lookup"><span data-stu-id="b56c0-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="b56c0-151">単一のフォレストまたはフォレスト間構成で、レプリケーションがアクセス制御リスト (ACL) によって制御されている場合は、DTE_IS_ACL_CAPABLE マクロを使用して、エントリがセキュリティ プリンシパルであるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="b56c0-152">フォレスト間構成では **、PR_DISPLAY_TYPEの** 値がDT_REMOTE_MAILUSER。</span><span class="sxs-lookup"><span data-stu-id="b56c0-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="b56c0-153">このプロパティのDTE_REMOTEを適用すると、リモート エントリの種類を取得できます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="b56c0-154">リモート エントリの可能な種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b56c0-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="b56c0-155">**リモート エントリの種類**</span><span class="sxs-lookup"><span data-stu-id="b56c0-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="b56c0-156">**値**</span><span class="sxs-lookup"><span data-stu-id="b56c0-156">**Value**</span></span>|<span data-ttu-id="b56c0-157">**説明**</span><span class="sxs-lookup"><span data-stu-id="b56c0-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b56c0-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="b56c0-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="b56c0-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="b56c0-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="b56c0-160">動的配布リスト。</span><span class="sxs-lookup"><span data-stu-id="b56c0-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="b56c0-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b56c0-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="b56c0-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b56c0-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b56c0-163">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="b56c0-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="b56c0-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="b56c0-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="b56c0-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="b56c0-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="b56c0-166">プリンターやプロジェクターなどの機器。</span><span class="sxs-lookup"><span data-stu-id="b56c0-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="b56c0-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b56c0-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="b56c0-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="b56c0-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="b56c0-169">メールボックスを持つユーザー。</span><span class="sxs-lookup"><span data-stu-id="b56c0-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="b56c0-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b56c0-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="b56c0-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="b56c0-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="b56c0-172">グローバル アドレス一覧のアドレス一覧エントリ。</span><span class="sxs-lookup"><span data-stu-id="b56c0-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="b56c0-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="b56c0-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="b56c0-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="b56c0-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="b56c0-175">会議室。</span><span class="sxs-lookup"><span data-stu-id="b56c0-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="b56c0-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b56c0-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b56c0-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="b56c0-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="b56c0-178">セキュリティ配布リスト。</span><span class="sxs-lookup"><span data-stu-id="b56c0-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="b56c0-179">単一フォレストとフォレスト間構成の両方で **、PR_DISPLAY_TYPE** の値が DT_DISTLIST と DTE_IS_REMOTE_VALID が false の場合は、このプロパティの値に DTE_LOCAL マクロを適用すると、配布リストの種類を取得できます。</span><span class="sxs-lookup"><span data-stu-id="b56c0-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="b56c0-180">使用できる配布リストの種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b56c0-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="b56c0-181">**配布リストの種類**</span><span class="sxs-lookup"><span data-stu-id="b56c0-181">**Type of Distribution List**</span></span>|<span data-ttu-id="b56c0-182">**値**</span><span class="sxs-lookup"><span data-stu-id="b56c0-182">**Value**</span></span>|<span data-ttu-id="b56c0-183">**説明**</span><span class="sxs-lookup"><span data-stu-id="b56c0-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b56c0-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b56c0-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="b56c0-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b56c0-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b56c0-186">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="b56c0-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="b56c0-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b56c0-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b56c0-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="b56c0-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="b56c0-189">セキュリティ配布リスト。</span><span class="sxs-lookup"><span data-stu-id="b56c0-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b56c0-190">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b56c0-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b56c0-191">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b56c0-191">Protocol specifications</span></span>

<span data-ttu-id="b56c0-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b56c0-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b56c0-193">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b56c0-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b56c0-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b56c0-195">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b56c0-196">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b56c0-196">Header files</span></span>

<span data-ttu-id="b56c0-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b56c0-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="b56c0-198">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b56c0-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="b56c0-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b56c0-199">Mapitags.h</span></span>
  
> <span data-ttu-id="b56c0-200">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b56c0-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b56c0-201">関連項目</span><span class="sxs-lookup"><span data-stu-id="b56c0-201">See also</span></span>



[<span data-ttu-id="b56c0-202">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b56c0-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b56c0-203">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b56c0-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b56c0-204">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b56c0-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b56c0-205">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b56c0-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

