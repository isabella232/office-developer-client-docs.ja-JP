---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350884"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="70907-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70907-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="70907-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70907-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70907-105">microsoft exchange server table オブジェクトへのアクセスをサポートします。特に、システムアクセス制御リスト (SACL) テーブルオブジェクトと、microsoft exchange server フォルダー上のルールテーブルオブジェクトへのアクセスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="70907-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="70907-106">このインターフェイスは、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスに似ていますが、sacl とルールを制御するために使用される Microsoft Exchange Server 固有の構造のサポートが追加されています。</span><span class="sxs-lookup"><span data-stu-id="70907-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70907-107">公開者:</span><span class="sxs-lookup"><span data-stu-id="70907-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="70907-108">なし</span><span class="sxs-lookup"><span data-stu-id="70907-108">None</span></span>  <br/> |
|<span data-ttu-id="70907-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="70907-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="70907-110">サーバーテーブルオブジェクト</span><span class="sxs-lookup"><span data-stu-id="70907-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="70907-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="70907-111">Called by:</span></span>  <br/> |<span data-ttu-id="70907-112">MAPI およびクライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="70907-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="70907-113">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="70907-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="70907-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="70907-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="70907-115">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="70907-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="70907-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="70907-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="70907-117">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="70907-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="70907-118">一括</span><span class="sxs-lookup"><span data-stu-id="70907-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="70907-119">v の順序</span><span class="sxs-lookup"><span data-stu-id="70907-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="70907-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="70907-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="70907-121">table オブジェクトで発生した最後のエラーについての情報を返します。</span><span class="sxs-lookup"><span data-stu-id="70907-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="70907-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="70907-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="70907-123">MAPI table オブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="70907-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="70907-124">modifytable</span><span class="sxs-lookup"><span data-stu-id="70907-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="70907-125">MAPI テーブルオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="70907-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="70907-126">**ルールテーブルを変更するために使用されるプロパティ**</span><span class="sxs-lookup"><span data-stu-id="70907-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="70907-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="70907-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70907-128">**PR_RULE_ACTIONS**([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-129">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-130">**PR_RULE_CONDITION**([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-132">**PR_RULE_ID**([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-133">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-134">**PR_RULE_LEVEL**([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-136">**PR_RULE_NAME**([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-138">**PR_RULE_PROVIDER**([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-140">**PR_RULE_PROVIDER_DATA**([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-142">**PR_RULE_SEQUENCE**([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-144">**PR_RULE_STATE**([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-146">**PR_RULE_USER_FLAGS**([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="70907-148">**SACL テーブルを変更するために使用されるプロパティ**</span><span class="sxs-lookup"><span data-stu-id="70907-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="70907-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="70907-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70907-150">**PR_MEMBER_ENTRYID**([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-152">**PR_MEMBER_ID**([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-154">**PR_MEMBER_NAME**([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="70907-156">**PR_MEMBER_RIGHTS**([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="70907-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="70907-157">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="70907-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70907-158">解説</span><span class="sxs-lookup"><span data-stu-id="70907-158">Remarks</span></span>

<span data-ttu-id="70907-159">**IExchangeModifyTable**インターフェイスを取得するには、folder オブジェクトの PT_OBJECT 型のプロパティに対して MAPI [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="70907-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="70907-160">**openproperty**メソッドを呼び出すときに、 _lpiid_パラメーターの値**IID_IExchangeModifyTable**を渡します。</span><span class="sxs-lookup"><span data-stu-id="70907-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70907-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="70907-161">See also</span></span>



[<span data-ttu-id="70907-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="70907-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

