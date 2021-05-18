---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407530"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="e857d-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e857d-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="e857d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e857d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e857d-105">フォーム ライブラリ内のフォームを管理します。</span><span class="sxs-lookup"><span data-stu-id="e857d-105">Manages forms in form libraries.</span></span> <span data-ttu-id="e857d-106">このインターフェイスは、アプリケーション固有のフォーム ライブラリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e857d-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e857d-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e857d-107">Header file:</span></span>  <br/> |<span data-ttu-id="e857d-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e857d-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e857d-109">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="e857d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e857d-110">フォーム コンテナー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e857d-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="e857d-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="e857d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e857d-112">フォーム ライブラリ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e857d-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="e857d-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e857d-113">Called by:</span></span>  <br/> |<span data-ttu-id="e857d-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e857d-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="e857d-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e857d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e857d-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="e857d-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="e857d-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="e857d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e857d-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="e857d-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e857d-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e857d-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e857d-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="e857d-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="e857d-121">フォームコンテナーにフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e857d-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="e857d-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="e857d-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="e857d-123">フォーム コンテナーから特定のフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="e857d-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="e857d-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="e857d-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="e857d-125">メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="e857d-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="e857d-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e857d-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="e857d-127">メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="e857d-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="e857d-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="e857d-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="e857d-129">フォーム コンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="e857d-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="e857d-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="e857d-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="e857d-131">フォーム コンテナーの表示名を返します。</span><span class="sxs-lookup"><span data-stu-id="e857d-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="e857d-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e857d-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="e857d-133">フォーム コンテナー オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="e857d-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e857d-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e857d-134">See also</span></span>



[<span data-ttu-id="e857d-135">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e857d-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

