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
ms.openlocfilehash: a21eecfb1bf3bc4f09fc5becb9a4a99a97193330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802715"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="0ef66-103">PidTagDisplayTypeEx 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ef66-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="0ef66-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ef66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ef66-105">グローバル アドレス一覧のエントリをテーブル内の行に表示する方法について、エントリの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ef66-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ef66-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0ef66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ef66-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="0ef66-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="0ef66-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0ef66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ef66-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="0ef66-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="0ef66-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0ef66-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ef66-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0ef66-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0ef66-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0ef66-112">Area:</span></span>  <br/> |<span data-ttu-id="0ef66-113">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="0ef66-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ef66-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0ef66-114">Remarks</span></span>

<span data-ttu-id="0ef66-115">このプロパティは、グローバル アドレス一覧での表示の方法について、エントリの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="0ef66-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) で表すことができないその他の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="0ef66-117">**PR_DISPLAY_TYPE**とこのプロパティの両方の値は、「dt _」で始まるし、Mapitags.h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="0ef66-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="0ef66-118">記載されていないすべての値は、MAPI 用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="0ef66-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="0ef66-119">クライアント アプリケーションは、新しい値を定義する必要がないと、文書化されていない値で対処するために準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ef66-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="0ef66-120">ローカル、リモート、またはセキュリティ制御などのオブジェクトの属性を判断するのに役立ついくつかのマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="0ef66-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="0ef66-121">これらのマクロは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-121">These macros include:</span></span> 
  
|<span data-ttu-id="0ef66-122">**マクロ**</span><span class="sxs-lookup"><span data-stu-id="0ef66-122">**Macro**</span></span>|<span data-ttu-id="0ef66-123">**値**</span><span class="sxs-lookup"><span data-stu-id="0ef66-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ef66-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="0ef66-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="0ef66-125">0x80000000)</span><span class="sxs-lookup"><span data-stu-id="0ef66-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="0ef66-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="0ef66-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="0ef66-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="0ef66-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="0ef66-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="0ef66-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="0ef66-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="0ef66-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="0ef66-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0ef66-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="0ef66-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="0ef66-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="0ef66-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="0ef66-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="0ef66-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="0ef66-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="0ef66-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="0ef66-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="0ef66-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="0ef66-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="0ef66-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="0ef66-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="0ef66-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="0ef66-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="0ef66-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="0ef66-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="0ef66-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="0ef66-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="0ef66-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="0ef66-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="0ef66-141">((ULONG) 0X00000007)</span><span class="sxs-lookup"><span data-stu-id="0ef66-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="0ef66-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="0ef66-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="0ef66-143">((ULONG) 0X00000008)</span><span class="sxs-lookup"><span data-stu-id="0ef66-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="0ef66-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0ef66-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="0ef66-145">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="0ef66-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="0ef66-146">これらのマクロを使用する方法について、いくつかのノートを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="0ef66-147">エントリは、別のフォレスト内のリモートのエントリであるかどうかを確認するには、エントリに DTE_FLAG_REMOTE_VALID フラグが設定されているかどうかを確認するには、このプロパティの値に DTE_IS_REMOTE_VALID マクロを適用します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="0ef66-148">リモート エントリがある場合を調べることができますし、リモート エントリの種類 DTE_REMOTE マクロを使用しています。</span><span class="sxs-lookup"><span data-stu-id="0ef66-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="0ef66-149">単一フォレストとフォレスト間の両方の構成では、 **PR_DISPLAY_TYPE**が DT_DISTLIST、および DTE_IS_REMOTE_VALID の値は、このプロパティの値にマクロ DTE_LOCAL を適用することができます、オブジェクトの種類を識別するためDT_DISTLIST (配布リスト) または DT_SEC_DISTLIST (セキュリティの配布リスト) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="0ef66-150">マクロ DTE_LOCAL を**PR_DISPLAY_TYPE_EX**の値に適用すると、DT_REMOTE_MAILUSER の種類を取得して、エントリがリモートのエントリとします。</span><span class="sxs-lookup"><span data-stu-id="0ef66-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="0ef66-151">単一フォレストまたはレプリケーションにアクセス制御リスト (ACL) では、制御されているフォレスト間の構成では、エントリがセキュリティ プリンシパルであるかどうかを確認するのには、DTE_IS_ACL_CAPABLE マクロを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ef66-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="0ef66-152">クロス フォレスト構成の場合、 **PR_DISPLAY_TYPE** DT_REMOTE_MAILUSER の値があります。</span><span class="sxs-lookup"><span data-stu-id="0ef66-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="0ef66-153">このプロパティの値にマクロ DTE_REMOTE を適用すると、リモートのエントリの種類を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="0ef66-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="0ef66-154">リモート エントリの種類、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="0ef66-155">**リモート エントリの種類**</span><span class="sxs-lookup"><span data-stu-id="0ef66-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="0ef66-156">**値**</span><span class="sxs-lookup"><span data-stu-id="0ef66-156">**Value**</span></span>|<span data-ttu-id="0ef66-157">**説明**</span><span class="sxs-lookup"><span data-stu-id="0ef66-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ef66-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="0ef66-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="0ef66-159">((ULONG) 0X00000003)</span><span class="sxs-lookup"><span data-stu-id="0ef66-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="0ef66-160">動的配布リストです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="0ef66-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0ef66-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="0ef66-162">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="0ef66-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="0ef66-163">配布リストです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="0ef66-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="0ef66-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="0ef66-165">((ULONG) 0X00000008)</span><span class="sxs-lookup"><span data-stu-id="0ef66-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="0ef66-166">プリンターやプロジェクターなどの機器です。</span><span class="sxs-lookup"><span data-stu-id="0ef66-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="0ef66-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="0ef66-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="0ef66-168">((ULONG) 0X00000000)</span><span class="sxs-lookup"><span data-stu-id="0ef66-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="0ef66-169">メールボックスを持つユーザーです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="0ef66-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="0ef66-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="0ef66-171">((ULONG) 0X00000000)</span><span class="sxs-lookup"><span data-stu-id="0ef66-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="0ef66-172">グローバル アドレス一覧にアドレス一覧エントリです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="0ef66-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="0ef66-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="0ef66-174">((ULONG) 0X00000007)</span><span class="sxs-lookup"><span data-stu-id="0ef66-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="0ef66-175">会議室です。</span><span class="sxs-lookup"><span data-stu-id="0ef66-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="0ef66-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0ef66-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="0ef66-177">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="0ef66-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="0ef66-178">配布リストのセキュリティです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="0ef66-179">構成の場合、 **PR_DISPLAY_TYPE**に DT_DISTLIST と DTE_IS_REMOTE_VALID の値が設定されているときは両方単一のフォレストとフォレスト間で、このプロパティの値に DTE_LOCAL マクロを適用することができます配布リストの種類を取得します。.</span><span class="sxs-lookup"><span data-stu-id="0ef66-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="0ef66-180">配布リストの種類、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="0ef66-181">**配布リストの種類**</span><span class="sxs-lookup"><span data-stu-id="0ef66-181">**Type of Distribution List**</span></span>|<span data-ttu-id="0ef66-182">**値**</span><span class="sxs-lookup"><span data-stu-id="0ef66-182">**Value**</span></span>|<span data-ttu-id="0ef66-183">**説明**</span><span class="sxs-lookup"><span data-stu-id="0ef66-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ef66-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0ef66-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="0ef66-185">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="0ef66-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="0ef66-186">配布リストです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="0ef66-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0ef66-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="0ef66-188">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="0ef66-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="0ef66-189">配布リストのセキュリティです。</span><span class="sxs-lookup"><span data-stu-id="0ef66-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0ef66-190">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0ef66-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ef66-191">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0ef66-191">Protocol specifications</span></span>

<span data-ttu-id="0ef66-192">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ef66-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ef66-193">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ef66-194">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ef66-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ef66-195">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ef66-196">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0ef66-196">Header files</span></span>

<span data-ttu-id="0ef66-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ef66-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ef66-198">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ef66-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ef66-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ef66-199">Mapitags.h</span></span>
  
> <span data-ttu-id="0ef66-200">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ef66-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ef66-201">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ef66-201">See also</span></span>



[<span data-ttu-id="0ef66-202">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ef66-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ef66-203">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ef66-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ef66-204">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0ef66-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ef66-205">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0ef66-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

