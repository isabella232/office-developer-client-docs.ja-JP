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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418107"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="a3d57-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3d57-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="a3d57-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3d57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3d57-105">microsoft exchange server table オブジェクトへのアクセスをサポートします。特に、システムアクセス制御リスト (SACL) テーブルオブジェクトと、microsoft exchange server フォルダー上のルールテーブルオブジェクトへのアクセスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a3d57-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="a3d57-106">このインターフェイスは、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスに似ていますが、sacl とルールを制御するために使用される Microsoft Exchange Server 固有の構造のサポートが追加されています。</span><span class="sxs-lookup"><span data-stu-id="a3d57-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3d57-107">公開者:</span><span class="sxs-lookup"><span data-stu-id="a3d57-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="a3d57-108">なし</span><span class="sxs-lookup"><span data-stu-id="a3d57-108">None</span></span>  <br/> |
|<span data-ttu-id="a3d57-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="a3d57-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3d57-110">サーバーテーブルオブジェクト</span><span class="sxs-lookup"><span data-stu-id="a3d57-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="a3d57-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a3d57-111">Called by:</span></span>  <br/> |<span data-ttu-id="a3d57-112">MAPI およびクライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="a3d57-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="a3d57-113">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="a3d57-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a3d57-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="a3d57-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="a3d57-115">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="a3d57-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="a3d57-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="a3d57-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="a3d57-117">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="a3d57-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="a3d57-118">一括</span><span class="sxs-lookup"><span data-stu-id="a3d57-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a3d57-119">v の順序</span><span class="sxs-lookup"><span data-stu-id="a3d57-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a3d57-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a3d57-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="a3d57-121">table オブジェクトで発生した最後のエラーについての情報を返します。</span><span class="sxs-lookup"><span data-stu-id="a3d57-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="a3d57-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="a3d57-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="a3d57-123">MAPI table オブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a3d57-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="a3d57-124">modifytable</span><span class="sxs-lookup"><span data-stu-id="a3d57-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="a3d57-125">MAPI テーブルオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="a3d57-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="a3d57-126">**ルールテーブルを変更するために使用されるプロパティ**</span><span class="sxs-lookup"><span data-stu-id="a3d57-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="a3d57-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="a3d57-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3d57-128">**PR_RULE_ACTIONS**([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-129">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-130">**PR_RULE_CONDITION**([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-132">**PR_RULE_ID**([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-133">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-134">**PR_RULE_LEVEL**([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-136">**PR_RULE_NAME**([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-138">**PR_RULE_PROVIDER**([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-140">**PR_RULE_PROVIDER_DATA**([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-142">**PR_RULE_SEQUENCE**([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-144">**PR_RULE_STATE**([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-146">**PR_RULE_USER_FLAGS**([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="a3d57-148">**SACL テーブルを変更するために使用されるプロパティ**</span><span class="sxs-lookup"><span data-stu-id="a3d57-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="a3d57-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="a3d57-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3d57-150">**PR_MEMBER_ENTRYID**([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-152">**PR_MEMBER_ID**([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-154">**PR_MEMBER_NAME**([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3d57-156">**PR_MEMBER_RIGHTS**([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3d57-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3d57-157">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a3d57-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3d57-158">注釈</span><span class="sxs-lookup"><span data-stu-id="a3d57-158">Remarks</span></span>

<span data-ttu-id="a3d57-159">**IExchangeModifyTable**インターフェイスを取得するには、folder オブジェクトの PT_OBJECT 型のプロパティに対して MAPI [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a3d57-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="a3d57-160">**openproperty**メソッドを呼び出すときに、 _lpiid_パラメーターの値**IID_IExchangeModifyTable**を渡します。</span><span class="sxs-lookup"><span data-stu-id="a3d57-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3d57-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3d57-161">See also</span></span>



[<span data-ttu-id="a3d57-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3d57-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

