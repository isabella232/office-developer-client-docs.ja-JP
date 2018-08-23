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
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800431"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="cd98d-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd98d-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="cd98d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cd98d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cd98d-105">Microsoft Exchange Server のテーブルのオブジェクトへのアクセスをサポートしています、具体的にはシステムへのアクセス制御リスト (SACL) テーブルのオブジェクトと、Microsoft Exchange Server フォルダーで table オブジェクトを除外します。</span><span class="sxs-lookup"><span data-stu-id="cd98d-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="cd98d-106">このインターフェイスのような[IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースが、Sacl と規則を制御するために使用されている Microsoft Exchange Server に固有の構造体のサポートの追加。</span><span class="sxs-lookup"><span data-stu-id="cd98d-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd98d-107">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="cd98d-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="cd98d-108">なし</span><span class="sxs-lookup"><span data-stu-id="cd98d-108">None</span></span>  <br/> |
|<span data-ttu-id="cd98d-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="cd98d-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd98d-110">サーバー テーブル オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cd98d-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="cd98d-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cd98d-111">Called by:</span></span>  <br/> |<span data-ttu-id="cd98d-112">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="cd98d-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="cd98d-113">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="cd98d-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cd98d-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="cd98d-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="cd98d-115">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="cd98d-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="cd98d-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="cd98d-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="cd98d-117">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="cd98d-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="cd98d-118">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="cd98d-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cd98d-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="cd98d-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cd98d-120">発生しました</span><span class="sxs-lookup"><span data-stu-id="cd98d-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="cd98d-121">Table オブジェクトには、最後に発生したエラーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="cd98d-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="cd98d-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="cd98d-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="cd98d-123">MAPI テーブルのオブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="cd98d-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="cd98d-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="cd98d-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="cd98d-125">MAPI テーブルのオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="cd98d-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="cd98d-126">**規則テーブルを変更するためのプロパティ**</span><span class="sxs-lookup"><span data-stu-id="cd98d-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="cd98d-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="cd98d-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd98d-128">**PR_RULE_ACTIONS**([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-129">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-130">**PR_RULE_CONDITION**([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-132">**PR_RULE_ID**([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-133">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-134">**PR_RULE_LEVEL**([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-136">**PR_RULE_NAME**([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-138">**PR_RULE_PROVIDER**([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-140">**PR_RULE_PROVIDER_DATA**([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-142">**PR_RULE_SEQUENCE**([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-144">**PR_RULE_STATE**([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-146">**PR_RULE_USER_FLAGS**([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="cd98d-148">**SACL のテーブルを変更するためのプロパティ**</span><span class="sxs-lookup"><span data-stu-id="cd98d-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="cd98d-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="cd98d-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd98d-150">**PR_MEMBER_ENTRYID**([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-152">**PR_MEMBER_ID**([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-154">**PR_MEMBER_NAME**([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd98d-156">**PR_MEMBER_RIGHTS**([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd98d-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd98d-157">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cd98d-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd98d-158">注釈</span><span class="sxs-lookup"><span data-stu-id="cd98d-158">Remarks</span></span>

<span data-ttu-id="cd98d-159">**IExchangeModifyTable**インターフェイスを取得するには、PT_OBJECT フォルダー オブジェクトの種類のプロパティに対して MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd98d-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="cd98d-160">**OpenProperty**メソッドを呼び出すときは、 **IID_IExchangeModifyTable** 、 _lpiid_パラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="cd98d-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd98d-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd98d-161">See also</span></span>



[<span data-ttu-id="cd98d-162">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cd98d-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

