---
title: imapisession IUnknown
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328288"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="26456-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26456-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="26456-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26456-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26456-105">MAPI ログオンセッションに関連付けられているオブジェクトを管理します。</span><span class="sxs-lookup"><span data-stu-id="26456-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26456-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="26456-106">Header file:</span></span>  <br/> |<span data-ttu-id="26456-107">mapix</span><span class="sxs-lookup"><span data-stu-id="26456-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="26456-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="26456-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="26456-109">Session オブジェクト</span><span class="sxs-lookup"><span data-stu-id="26456-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="26456-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="26456-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="26456-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="26456-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="26456-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="26456-112">Called by:</span></span>  <br/> |<span data-ttu-id="26456-113">クライアントアプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="26456-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="26456-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="26456-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="26456-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="26456-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="26456-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="26456-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="26456-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="26456-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="26456-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="26456-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="26456-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="26456-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="26456-120">前のセッションエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="26456-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="26456-121">getmsgstorestable</span><span class="sxs-lookup"><span data-stu-id="26456-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="26456-122">セッションプロファイル内のすべてのメッセージストアに関する情報を含むメッセージストアテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="26456-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="26456-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="26456-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="26456-124">メッセージストアを開き、さらにアクセスするための[IMsgStore](imsgstoreimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="26456-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="26456-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="26456-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="26456-126">MAPI 統合アドレス帳を開き、さらにアクセスするために[IAddrBook](iaddrbookimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="26456-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="26456-127">openプロファイル '</span><span class="sxs-lookup"><span data-stu-id="26456-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="26456-128">現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="26456-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="26456-129">getstatustable</span><span class="sxs-lookup"><span data-stu-id="26456-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="26456-130">状態テーブル (セッション内のすべての MAPI リソースに関する情報を含むテーブル) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="26456-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="26456-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="26456-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="26456-132">オブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="26456-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="26456-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="26456-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="26456-134">2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="26456-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="26456-135">助言</span><span class="sxs-lookup"><span data-stu-id="26456-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="26456-136">セッションに影響を与える指定したイベントの通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="26456-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="26456-137">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="26456-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="26456-138">**アドバイズ**メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="26456-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="26456-139">**messageoptions**</span><span class="sxs-lookup"><span data-stu-id="26456-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="26456-140">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="26456-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="26456-141">**querydefaultmessageopt**</span><span class="sxs-lookup"><span data-stu-id="26456-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="26456-142">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="26456-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="26456-143">enumadrtypes</span><span class="sxs-lookup"><span data-stu-id="26456-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="26456-144">現在は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="26456-144">Deprecated.</span></span> <span data-ttu-id="26456-145">セッション内のすべてのトランスポートプロバイダーで処理できるアドレスの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="26456-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="26456-146">queryidentity</span><span class="sxs-lookup"><span data-stu-id="26456-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="26456-147">セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="26456-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="26456-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="26456-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="26456-149">MAPI セッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="26456-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="26456-150">setdefaultstore</span><span class="sxs-lookup"><span data-stu-id="26456-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="26456-151">セッションの既定のメッセージストアとしてメッセージストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="26456-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="26456-152">adminservices</span><span class="sxs-lookup"><span data-stu-id="26456-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="26456-153">メッセージサービスに変更を加えるための[IMsgServiceAdmin](imsgserviceadminiunknown.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="26456-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="26456-154">showform</span><span class="sxs-lookup"><span data-stu-id="26456-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="26456-155">フォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="26456-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="26456-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="26456-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="26456-157">**showform**メソッドがメッセージにアクセスするために使用する数値トークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="26456-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26456-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="26456-158">See also</span></span>



[<span data-ttu-id="26456-159">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="26456-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

