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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800431"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="2ef09-103">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ef09-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="2ef09-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ef09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ef09-105">Microsoft Exchange Server のテーブルのオブジェクトへのアクセスをサポートしています、具体的にはシステムへのアクセス制御リスト (SACL) テーブルのオブジェクトと、Microsoft Exchange Server フォルダーで table オブジェクトを除外します。</span><span class="sxs-lookup"><span data-stu-id="2ef09-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="2ef09-106">このインターフェイスのような[IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースが、Sacl と規則を制御するために使用されている Microsoft Exchange Server に固有の構造体のサポートの追加。</span><span class="sxs-lookup"><span data-stu-id="2ef09-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ef09-107">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="2ef09-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="2ef09-108">なし</span><span class="sxs-lookup"><span data-stu-id="2ef09-108">None</span></span>  <br/> |
|<span data-ttu-id="2ef09-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2ef09-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ef09-110">サーバー テーブル オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2ef09-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="2ef09-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2ef09-111">Called by:</span></span>  <br/> |<span data-ttu-id="2ef09-112">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2ef09-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="2ef09-113">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="2ef09-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2ef09-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="2ef09-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="2ef09-115">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="2ef09-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="2ef09-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="2ef09-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="2ef09-117">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="2ef09-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="2ef09-118">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="2ef09-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2ef09-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="2ef09-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2ef09-120">発生しました</span><span class="sxs-lookup"><span data-stu-id="2ef09-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="2ef09-121">Table オブジェクトには、最後に発生したエラーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="2ef09-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="2ef09-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="2ef09-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="2ef09-123">MAPI テーブルのオブジェクトのインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2ef09-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="2ef09-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="2ef09-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="2ef09-125">MAPI テーブルのオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="2ef09-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="2ef09-126">**規則テーブルを変更するためのプロパティ**</span><span class="sxs-lookup"><span data-stu-id="2ef09-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="2ef09-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="2ef09-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ef09-128">**PR_RULE_ACTIONS**([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-129">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-130">**PR_RULE_CONDITION**([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-131">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-132">**PR_RULE_ID**([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-133">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-134">**PR_RULE_LEVEL**([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-135">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-136">**PR_RULE_NAME**([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-137">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-138">**PR_RULE_PROVIDER**([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-139">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-140">**PR_RULE_PROVIDER_DATA**([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-141">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-142">**PR_RULE_SEQUENCE**([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-143">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-144">**PR_RULE_STATE**([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-145">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-146">**PR_RULE_USER_FLAGS**([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-147">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="2ef09-148">**SACL のテーブルを変更するためのプロパティ**</span><span class="sxs-lookup"><span data-stu-id="2ef09-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="2ef09-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="2ef09-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ef09-150">**PR_MEMBER_ENTRYID**([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-151">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-152">**PR_MEMBER_ID**([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-153">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-154">**PR_MEMBER_NAME**([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-155">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="2ef09-156">**PR_MEMBER_RIGHTS**([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ef09-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2ef09-157">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="2ef09-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ef09-158">備考</span><span class="sxs-lookup"><span data-stu-id="2ef09-158">Remarks</span></span>

<span data-ttu-id="2ef09-159">**IExchangeModifyTable**インターフェイスを取得するには、PT_OBJECT フォルダー オブジェクトの種類のプロパティに対して MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2ef09-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="2ef09-160">**OpenProperty**メソッドを呼び出すときは、 **IID_IExchangeModifyTable** 、 _lpiid_パラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="2ef09-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ef09-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ef09-161">See also</span></span>



[<span data-ttu-id="2ef09-162">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2ef09-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

