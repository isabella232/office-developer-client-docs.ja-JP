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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360775"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="a69b7-103">PidTagDisplayTypeEx 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a69b7-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="a69b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a69b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a69b7-105">グローバルアドレス一覧のテーブルの行にエントリを表示する方法についての、エントリの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a69b7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a69b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a69b7-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="a69b7-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="a69b7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a69b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a69b7-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="a69b7-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="a69b7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a69b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="a69b7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a69b7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a69b7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a69b7-112">Area:</span></span>  <br/> |<span data-ttu-id="a69b7-113">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="a69b7-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a69b7-114">解説</span><span class="sxs-lookup"><span data-stu-id="a69b7-114">Remarks</span></span>

<span data-ttu-id="a69b7-115">このプロパティは、エントリの種類をグローバルアドレス一覧にどのように表示するかについて指定します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="a69b7-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) では表現できない追加情報が提供されています。</span><span class="sxs-lookup"><span data-stu-id="a69b7-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a69b7-117">**PR_DISPLAY_TYPE**およびこのプロパティの両方の値は、"DT_" で始まり、Mapitags で定義されます。</span><span class="sxs-lookup"><span data-stu-id="a69b7-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="a69b7-118">文書化されていないすべての値は MAPI 用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="a69b7-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="a69b7-119">クライアントアプリケーションは、新しい値を定義せず、文書化されていない値を処理するために準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a69b7-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="a69b7-120">オブジェクトの属性をローカル、リモート、セキュリティ制御のいずれであるかを判断するのに役立つマクロがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="a69b7-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="a69b7-121">これらのマクロは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a69b7-121">These macros include:</span></span> 
  
|<span data-ttu-id="a69b7-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="a69b7-122">**Macro**</span></span>|<span data-ttu-id="a69b7-123">**値**</span><span class="sxs-lookup"><span data-stu-id="a69b7-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a69b7-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="a69b7-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="a69b7-125">0x80000000</span><span class="sxs-lookup"><span data-stu-id="a69b7-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="a69b7-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="a69b7-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="a69b7-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="a69b7-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="a69b7-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="a69b7-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="a69b7-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="a69b7-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="a69b7-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="a69b7-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="a69b7-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="a69b7-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="a69b7-132">DTE_IS_REMOTE_VALID (v)</span><span class="sxs-lookup"><span data-stu-id="a69b7-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="a69b7-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="a69b7-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="a69b7-134">DTE_IS_ACL_CAPABLE (v)</span><span class="sxs-lookup"><span data-stu-id="a69b7-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="a69b7-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="a69b7-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="a69b7-136">DTE_REMOTE (v)</span><span class="sxs-lookup"><span data-stu-id="a69b7-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="a69b7-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="a69b7-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="a69b7-138">DTE_LOCAL (v)</span><span class="sxs-lookup"><span data-stu-id="a69b7-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="a69b7-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="a69b7-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="a69b7-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="a69b7-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="a69b7-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="a69b7-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="a69b7-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="a69b7-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="a69b7-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a69b7-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="a69b7-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="a69b7-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="a69b7-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="a69b7-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="a69b7-146">これらのマクロの使用方法に関するいくつかの注意事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="a69b7-147">エントリが別のフォレスト内のリモートエントリであるかどうかを確認するには、DTE_IS_REMOTE_VALID マクロをこのプロパティの値に適用して、DTE_FLAG_REMOTE_VALID フラグがエントリに設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="a69b7-148">リモートエントリの場合は、DTE_REMOTE マクロを使用してリモートエントリの種類を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="a69b7-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="a69b7-149">**PR_DISPLAY_TYPE**の値が DT_DISTLIST で、かつ DTE_IS_REMOTE_VALID が false の場合は、単一フォレスト構成とフォレスト間の構成の両方で、このプロパティの値にマクロ DTE_LOCAL を適用すると、オブジェクトの種類をさらに詳しく識別できます。DT_DISTLIST (配布リスト) または DT_SEC_DISTLIST (セキュリティ配布リスト) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="a69b7-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="a69b7-150">マクロ DTE_LOCAL を**PR_DISPLAY_TYPE_EX**の値に適用し、DT_REMOTE_MAILUSER 型を返す場合、エントリはリモートエントリです。</span><span class="sxs-lookup"><span data-stu-id="a69b7-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="a69b7-151">単一のフォレスト、またはレプリケーションがアクセス制御リスト (ACL) によって制御されているフォレスト間の構成では、DTE_IS_ACL_CAPABLE マクロを使用して、エントリがセキュリティプリンシパルであるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="a69b7-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="a69b7-152">フォレスト間の構成では、 **PR_DISPLAY_TYPE**は DT_REMOTE_MAILUSER という値を持っています。</span><span class="sxs-lookup"><span data-stu-id="a69b7-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="a69b7-153">このプロパティの値にマクロ DTE_REMOTE を適用すると、リモートエントリの種類を取得することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="a69b7-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="a69b7-154">リモートエントリには、次のような種類があります。</span><span class="sxs-lookup"><span data-stu-id="a69b7-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="a69b7-155">**リモートエントリの種類**</span><span class="sxs-lookup"><span data-stu-id="a69b7-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="a69b7-156">**値**</span><span class="sxs-lookup"><span data-stu-id="a69b7-156">**Value**</span></span>|<span data-ttu-id="a69b7-157">**説明**</span><span class="sxs-lookup"><span data-stu-id="a69b7-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a69b7-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="a69b7-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="a69b7-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="a69b7-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="a69b7-160">動的配布リスト。</span><span class="sxs-lookup"><span data-stu-id="a69b7-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="a69b7-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="a69b7-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="a69b7-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a69b7-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="a69b7-163">配布リスト</span><span class="sxs-lookup"><span data-stu-id="a69b7-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="a69b7-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="a69b7-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="a69b7-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a69b7-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="a69b7-166">装置 (例: プリンターやプロジェクター)。</span><span class="sxs-lookup"><span data-stu-id="a69b7-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="a69b7-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="a69b7-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="a69b7-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="a69b7-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="a69b7-169">メールボックスを持つユーザー。</span><span class="sxs-lookup"><span data-stu-id="a69b7-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="a69b7-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="a69b7-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="a69b7-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="a69b7-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="a69b7-172">グローバルアドレス一覧のアドレス一覧のエントリ。</span><span class="sxs-lookup"><span data-stu-id="a69b7-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="a69b7-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="a69b7-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="a69b7-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="a69b7-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="a69b7-175">会議室。</span><span class="sxs-lookup"><span data-stu-id="a69b7-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="a69b7-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="a69b7-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="a69b7-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="a69b7-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="a69b7-178">セキュリティ配布リスト。</span><span class="sxs-lookup"><span data-stu-id="a69b7-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="a69b7-179">**PR_DISPLAY_TYPE**の値が DT_DISTLIST で、かつ DTE_IS_REMOTE_VALID が false の場合、単一フォレストとフォレスト間の構成の両方で、このプロパティの値に DTE_LOCAL マクロを適用すると、配布リストの種類を取得できるようになります。.</span><span class="sxs-lookup"><span data-stu-id="a69b7-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="a69b7-180">配布リストには、次の種類があります。</span><span class="sxs-lookup"><span data-stu-id="a69b7-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="a69b7-181">**配布リストの種類**</span><span class="sxs-lookup"><span data-stu-id="a69b7-181">**Type of Distribution List**</span></span>|<span data-ttu-id="a69b7-182">**値**</span><span class="sxs-lookup"><span data-stu-id="a69b7-182">**Value**</span></span>|<span data-ttu-id="a69b7-183">**説明**</span><span class="sxs-lookup"><span data-stu-id="a69b7-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a69b7-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="a69b7-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="a69b7-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a69b7-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="a69b7-186">配布リスト</span><span class="sxs-lookup"><span data-stu-id="a69b7-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="a69b7-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="a69b7-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="a69b7-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="a69b7-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="a69b7-189">セキュリティ配布リスト。</span><span class="sxs-lookup"><span data-stu-id="a69b7-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a69b7-190">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a69b7-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a69b7-191">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a69b7-191">Protocol specifications</span></span>

<span data-ttu-id="a69b7-192">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a69b7-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a69b7-193">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a69b7-194">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a69b7-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a69b7-195">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a69b7-196">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a69b7-196">Header files</span></span>

<span data-ttu-id="a69b7-197">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a69b7-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="a69b7-198">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a69b7-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="a69b7-199">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a69b7-199">Mapitags.h</span></span>
  
> <span data-ttu-id="a69b7-200">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a69b7-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a69b7-201">関連項目</span><span class="sxs-lookup"><span data-stu-id="a69b7-201">See also</span></span>



[<span data-ttu-id="a69b7-202">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a69b7-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a69b7-203">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a69b7-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a69b7-204">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a69b7-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a69b7-205">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a69b7-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

