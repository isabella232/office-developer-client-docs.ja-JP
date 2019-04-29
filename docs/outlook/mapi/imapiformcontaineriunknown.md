---
title: imapiformcontainer IUnknown
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
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="4ddb6-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4ddb6-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="4ddb6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ddb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ddb6-105">フォームライブラリ内のフォームを管理します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-105">Manages forms in form libraries.</span></span> <span data-ttu-id="4ddb6-106">このインターフェイスは、アプリケーション固有のフォームライブラリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ddb6-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4ddb6-107">Header file:</span></span>  <br/> |<span data-ttu-id="4ddb6-108">Mapiform</span><span class="sxs-lookup"><span data-stu-id="4ddb6-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4ddb6-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="4ddb6-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="4ddb6-110">Form container オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4ddb6-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="4ddb6-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="4ddb6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ddb6-112">フォームライブラリプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4ddb6-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="4ddb6-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4ddb6-113">Called by:</span></span>  <br/> |<span data-ttu-id="4ddb6-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4ddb6-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="4ddb6-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="4ddb6-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4ddb6-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="4ddb6-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="4ddb6-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="4ddb6-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="4ddb6-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="4ddb6-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4ddb6-119">v の順序</span><span class="sxs-lookup"><span data-stu-id="4ddb6-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4ddb6-120">installform</span><span class="sxs-lookup"><span data-stu-id="4ddb6-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="4ddb6-121">フォームをフォームコンテナーにインストールします。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="4ddb6-122">removeform</span><span class="sxs-lookup"><span data-stu-id="4ddb6-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="4ddb6-123">フォームコンテナーから特定のフォームを削除します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="4ddb6-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="4ddb6-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="4ddb6-125">メッセージクラスをフォームコンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="4ddb6-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="4ddb6-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="4ddb6-127">フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="4ddb6-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="4ddb6-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="4ddb6-129">フォームコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="4ddb6-130">getdisplay</span><span class="sxs-lookup"><span data-stu-id="4ddb6-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="4ddb6-131">フォームコンテナーの表示名を返します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="4ddb6-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="4ddb6-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="4ddb6-133">form container オブジェクトに発生する前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="4ddb6-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ddb6-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ddb6-134">See also</span></span>



[<span data-ttu-id="4ddb6-135">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="4ddb6-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

