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
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="3d5d2-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d5d2-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="3d5d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d5d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d5d2-105">システム アクセス制御Microsoft Exchange Server(SACL) テーブル オブジェクトおよびルール テーブル オブジェクトへのアクセスをサポートします。Microsoft Exchange Serverします。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="3d5d2-106">このインターフェイスは[IMAPITable : IUnknown](imapitableiunknown.md)インターフェイスに似ているが、SACL とルールを制御するために使用される Microsoft Exchange Server 固有の構造のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d5d2-107">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="3d5d2-108">なし</span><span class="sxs-lookup"><span data-stu-id="3d5d2-108">None</span></span>  <br/> |
|<span data-ttu-id="3d5d2-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="3d5d2-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="3d5d2-110">サーバー テーブル オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3d5d2-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="3d5d2-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3d5d2-111">Called by:</span></span>  <br/> |<span data-ttu-id="3d5d2-112">MAPI およびクライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3d5d2-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="3d5d2-113">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="3d5d2-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3d5d2-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="3d5d2-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="3d5d2-115">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="3d5d2-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="3d5d2-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="3d5d2-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="3d5d2-117">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="3d5d2-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="3d5d2-118">Transacted</span><span class="sxs-lookup"><span data-stu-id="3d5d2-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3d5d2-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3d5d2-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3d5d2-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3d5d2-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="3d5d2-121">テーブル オブジェクトで発生した最後のエラーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="3d5d2-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="3d5d2-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="3d5d2-123">MAPI テーブル オブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="3d5d2-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="3d5d2-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="3d5d2-125">MAPI テーブル オブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="3d5d2-126">**ルール テーブルの変更に使用されるプロパティ**</span><span class="sxs-lookup"><span data-stu-id="3d5d2-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="3d5d2-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="3d5d2-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d5d2-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-129">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-133">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-147">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="3d5d2-148">**SACL テーブルの変更に使用されるプロパティ**</span><span class="sxs-lookup"><span data-stu-id="3d5d2-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="3d5d2-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="3d5d2-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d5d2-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d5d2-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d5d2-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d5d2-157">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3d5d2-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d5d2-158">注釈</span><span class="sxs-lookup"><span data-stu-id="3d5d2-158">Remarks</span></span>

<span data-ttu-id="3d5d2-159">**IExchangeModifyTable** インターフェイスを取得するには、フォルダー オブジェクトの種類 PT_OBJECT のプロパティで [MAPI IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="3d5d2-160">**OpenProperty メソッドを呼び出す** 場合は、lpiid パラメーター **IID_IExchangeModifyTable値**_を渡_ します。</span><span class="sxs-lookup"><span data-stu-id="3d5d2-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d5d2-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d5d2-161">See also</span></span>



[<span data-ttu-id="3d5d2-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3d5d2-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

