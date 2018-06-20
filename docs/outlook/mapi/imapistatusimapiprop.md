---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800719"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="9742f-103">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9742f-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="9742f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9742f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9742f-105">MAPI サブシステム、内蔵のアドレス帳、および MAPI スプーラーに関するステータス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9742f-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="9742f-106">サービス プロバイダーは、独自のステータスに関する情報を提供する**IMAPIStatus**を実装します。</span><span class="sxs-lookup"><span data-stu-id="9742f-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9742f-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9742f-107">Header file:</span></span>  <br/> |<span data-ttu-id="9742f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9742f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9742f-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="9742f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="9742f-110">ステータス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9742f-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="9742f-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9742f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="9742f-112">サービス プロバイダーおよび MAPI</span><span class="sxs-lookup"><span data-stu-id="9742f-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="9742f-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9742f-113">Called by:</span></span>  <br/> |<span data-ttu-id="9742f-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9742f-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="9742f-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="9742f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9742f-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="9742f-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="9742f-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="9742f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="9742f-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="9742f-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="9742f-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="9742f-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="9742f-120">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="9742f-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9742f-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="9742f-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9742f-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="9742f-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="9742f-123">MAPI リソースまたはサービス プロバイダーの使用可能な外部のステータス情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="9742f-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="9742f-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="9742f-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="9742f-125">サービス プロバイダーの構成を変更するユーザーを有効にするプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="9742f-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="9742f-126">パスワードの変更</span><span class="sxs-lookup"><span data-stu-id="9742f-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="9742f-127">ユーザー インターフェイスを表示せずには、サービス プロバイダーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="9742f-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="9742f-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9742f-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="9742f-129">送信またはアップロードまたはダウンロードをすぐに受信を待機しているすべてのメッセージを強制的にします。</span><span class="sxs-lookup"><span data-stu-id="9742f-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="9742f-130">**必要なプロパティ**</span><span class="sxs-lookup"><span data-stu-id="9742f-130">**Required properties**</span></span>|<span data-ttu-id="9742f-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="9742f-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9742f-132">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-133">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="9742f-134">**PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-135">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="9742f-136">**PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-137">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="9742f-138">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-139">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="9742f-140">**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-141">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="9742f-142">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-143">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="9742f-144">**PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9742f-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9742f-145">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="9742f-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9742f-146">備考</span><span class="sxs-lookup"><span data-stu-id="9742f-146">Remarks</span></span>

<span data-ttu-id="9742f-147">MAPI が実装している状態のオブジェクトでは、次のメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9742f-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="9742f-148">**ステータス オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="9742f-148">**Status object**</span></span>|<span data-ttu-id="9742f-149">**サポートされている方法**</span><span class="sxs-lookup"><span data-stu-id="9742f-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9742f-150">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="9742f-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="9742f-151">**ValidateState**のみ</span><span class="sxs-lookup"><span data-stu-id="9742f-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="9742f-152">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="9742f-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="9742f-153">**ValidateState**のみ</span><span class="sxs-lookup"><span data-stu-id="9742f-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="9742f-154">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="9742f-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="9742f-155">**ValidateState**と**FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="9742f-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="9742f-156">MAPI を実装する状態オブジェクトは、 [IMAPIProp](imapipropiunknown.md)インターフェイスのメソッドの読み取り専用バージョンが存在し、 **ValidateState**メソッドをサポートするためには必要です。</span><span class="sxs-lookup"><span data-stu-id="9742f-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="9742f-157">トランスポート プロバイダーでは、 **FlushQueues**もサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9742f-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="9742f-158">すべてのプロバイダーは、 **SettingsDialog**; をサポートする必要があります。**パスワードの変更**はオプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9742f-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="9742f-159">クライアントは、構成を実行して、セッションの状態については、状態オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="9742f-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="9742f-160">状態オブジェクトにアクセスするには、ログオンするサービス プロバイダー オブジェクトの**OpenStatusEntry**メソッドまたは状態オブジェクトを取得するために[IMAPISession::GetStatusTable](imapisession-getstatustable.md)メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="9742f-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9742f-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="9742f-161">See also</span></span>



[<span data-ttu-id="9742f-162">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9742f-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

