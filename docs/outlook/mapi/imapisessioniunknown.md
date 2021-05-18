---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413382"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="89f78-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89f78-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="89f78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89f78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89f78-105">MAPI ログオン セッションに関連付けられているオブジェクトを管理します。</span><span class="sxs-lookup"><span data-stu-id="89f78-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89f78-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="89f78-106">Header file:</span></span>  <br/> |<span data-ttu-id="89f78-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="89f78-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="89f78-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="89f78-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="89f78-109">セッション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="89f78-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="89f78-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="89f78-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="89f78-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="89f78-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="89f78-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="89f78-112">Called by:</span></span>  <br/> |<span data-ttu-id="89f78-113">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="89f78-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="89f78-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="89f78-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="89f78-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="89f78-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="89f78-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="89f78-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="89f78-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="89f78-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="89f78-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="89f78-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="89f78-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="89f78-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="89f78-120">前のセッション エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="89f78-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="89f78-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="89f78-122">セッション プロファイル内のすべてのメッセージ ストアに関する情報を含むメッセージ ストア テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="89f78-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="89f78-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="89f78-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="89f78-124">メッセージ ストアを開き、さらにアクセスする [IMsgStore ポインター](imsgstoreimapiprop.md) を返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="89f78-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="89f78-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="89f78-126">MAPI 統合アドレス帳を開き [、IAddrBook](iaddrbookimapiprop.md) ポインターを返してさらにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="89f78-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="89f78-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="89f78-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="89f78-128">現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="89f78-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="89f78-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="89f78-130">セッション内のすべての MAPI リソースに関する情報を含むテーブルである状態テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="89f78-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="89f78-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="89f78-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="89f78-132">オブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="89f78-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="89f78-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="89f78-134">2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="89f78-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="89f78-135">アドバイス</span><span class="sxs-lookup"><span data-stu-id="89f78-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="89f78-136">セッションに影響を与える指定されたイベントの通知を受信するために登録します。</span><span class="sxs-lookup"><span data-stu-id="89f78-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="89f78-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="89f78-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="89f78-138">Advise メソッドの呼び出しで以前に設定された通知の送信を **キャンセル** します。</span><span class="sxs-lookup"><span data-stu-id="89f78-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="89f78-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="89f78-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="89f78-140">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="89f78-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="89f78-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="89f78-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="89f78-142">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="89f78-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="89f78-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="89f78-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="89f78-144">非推奨。</span><span class="sxs-lookup"><span data-stu-id="89f78-144">Deprecated.</span></span> <span data-ttu-id="89f78-145">セッション内のすべてのトランスポート プロバイダーが処理できるアドレスの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="89f78-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="89f78-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="89f78-147">セッションのプライマリ ID を提供するオブジェクトのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="89f78-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="89f78-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="89f78-149">MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="89f78-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="89f78-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="89f78-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="89f78-151">セッションの既定のメッセージ ストアとしてメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="89f78-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="89f78-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="89f78-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="89f78-153">メッセージ サービスを [変更する IMsgServiceAdmin](imsgserviceadminiunknown.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="89f78-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="89f78-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="89f78-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="89f78-155">フォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="89f78-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="89f78-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="89f78-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="89f78-157">**ShowForm** メソッドがメッセージにアクセスするために使用する数値トークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="89f78-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89f78-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="89f78-158">See also</span></span>



[<span data-ttu-id="89f78-159">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="89f78-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

