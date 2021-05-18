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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408300"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="a01ac-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a01ac-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="a01ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a01ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a01ac-105">MAPI サブシステム、統合アドレス帳、および MAPI スプーラーに関する状態情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="a01ac-106">サービス プロバイダーは **IMAPIStatus を実装して、** 独自の状態に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a01ac-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a01ac-107">Header file:</span></span>  <br/> |<span data-ttu-id="a01ac-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a01ac-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a01ac-109">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="a01ac-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a01ac-110">状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a01ac-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="a01ac-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="a01ac-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a01ac-112">サービス プロバイダーと MAPI</span><span class="sxs-lookup"><span data-stu-id="a01ac-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="a01ac-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a01ac-113">Called by:</span></span>  <br/> |<span data-ttu-id="a01ac-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a01ac-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="a01ac-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="a01ac-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a01ac-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="a01ac-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="a01ac-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="a01ac-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a01ac-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="a01ac-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="a01ac-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="a01ac-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="a01ac-120">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="a01ac-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a01ac-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="a01ac-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a01ac-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="a01ac-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="a01ac-123">MAPI リソースまたはサービス プロバイダーで使用可能な外部状態情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="a01ac-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="a01ac-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="a01ac-125">ユーザーがサービス プロバイダーの構成を変更できるプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="a01ac-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="a01ac-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="a01ac-127">ユーザー インターフェイスを表示せずにサービス プロバイダーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="a01ac-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a01ac-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="a01ac-129">送信または受信を待機しているすべてのメッセージを、すぐにアップロードまたはダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a01ac-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="a01ac-130">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="a01ac-130">**Required properties**</span></span>|<span data-ttu-id="a01ac-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="a01ac-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a01ac-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-133">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="a01ac-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="a01ac-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-135">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="a01ac-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="a01ac-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a01ac-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="a01ac-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-139">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a01ac-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="a01ac-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-141">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a01ac-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="a01ac-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a01ac-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="a01ac-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a01ac-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a01ac-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="a01ac-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a01ac-146">注釈</span><span class="sxs-lookup"><span data-stu-id="a01ac-146">Remarks</span></span>

<span data-ttu-id="a01ac-147">MAPI が実装する状態オブジェクトは、次のメソッドをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a01ac-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="a01ac-148">**Status オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="a01ac-148">**Status object**</span></span>|<span data-ttu-id="a01ac-149">**サポートされているメソッド**</span><span class="sxs-lookup"><span data-stu-id="a01ac-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a01ac-150">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="a01ac-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="a01ac-151">**ValidateState** のみ</span><span class="sxs-lookup"><span data-stu-id="a01ac-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="a01ac-152">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="a01ac-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="a01ac-153">**ValidateState** のみ</span><span class="sxs-lookup"><span data-stu-id="a01ac-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="a01ac-154">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="a01ac-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="a01ac-155">**ValidateState** と **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="a01ac-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="a01ac-156">MAPI が実装する状態オブジェクトは [、IMAPIProp](imapipropiunknown.md) インターフェイスのメソッドの読み取り専用バージョンを持ち **、ValidateState** メソッドをサポートするために必要です。</span><span class="sxs-lookup"><span data-stu-id="a01ac-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="a01ac-157">トランスポート プロバイダーは **、FlushQueues もサポートする必要があります**。</span><span class="sxs-lookup"><span data-stu-id="a01ac-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="a01ac-158">すべてのプロバイダーが **SettingsDialog をサポートする必要があります**。 **ChangePassword のサポートは** オプションです。</span><span class="sxs-lookup"><span data-stu-id="a01ac-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="a01ac-159">クライアントは、状態オブジェクトを使用して構成を実行し、セッションの状態について学習します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="a01ac-160">サービス プロバイダー ログオン オブジェクトの **OpenStatusEntry** メソッドまたは [IMAPISession::GetStatusTable](imapisession-getstatustable.md) メソッドを呼び出して、状態オブジェクトにアクセスして、状態オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="a01ac-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a01ac-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="a01ac-161">See also</span></span>



[<span data-ttu-id="a01ac-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="a01ac-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

