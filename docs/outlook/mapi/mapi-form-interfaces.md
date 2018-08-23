---
title: MAPI フォーム インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8452a6e49059dd0912f1efffef7e749afd6cdf6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801358"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="9ce41-103">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ce41-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="9ce41-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ce41-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ce41-105">MAPI では、フォームに関連する次のインタ フェースを定義します。</span><span class="sxs-lookup"><span data-stu-id="9ce41-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="9ce41-106">**インターフェイス名**</span><span class="sxs-lookup"><span data-stu-id="9ce41-106">**Interface name**</span></span>|<span data-ttu-id="9ce41-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="9ce41-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ce41-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="9ce41-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="9ce41-109">フォーム オブジェクトを操作し、フォームのオブジェクトのコマンドを処理します。</span><span class="sxs-lookup"><span data-stu-id="9ce41-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9ce41-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="9ce41-111">フォーム オブジェクトが次のメッセージを処理することができ、フォーム オブジェクトの次または前の状態を変更するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9ce41-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="9ce41-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="9ce41-113">インストール、アンインストール、および特定のフォームのコンテナーに対するフォーム サーバーの解像度をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9ce41-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="9ce41-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="9ce41-115">サーバーの構成可能な実行時のフォームの使用をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9ce41-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="9ce41-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="9ce41-117">メッセージ クラスに特有のプロパティを操作するクライアント アプリケーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9ce41-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="9ce41-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="9ce41-119">フォームのサーバーに関する情報を取得するクライアント アプリケーション、フォームのサーバーをアクティブにでき、メッセージング システムでは、フォームのサーバーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="9ce41-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="9ce41-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="9ce41-121">フォーム オブジェクトに関連付けられているメッセージを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9ce41-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="9ce41-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="9ce41-123">フォーム オブジェクトでイベントが発生するクライアント アプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="9ce41-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="9ce41-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="9ce41-125">フォーム オブジェクトで、次、前、および削除のコマンドに応答する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ce41-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="9ce41-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="9ce41-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="9ce41-127">保存、初期化、およびメッセージの記憶域との間に、フォーム オブジェクトを読み込むに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ce41-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="9ce41-128">MAPI フォームのインターフェイスのメソッドに関する詳細については、これらのインタ フェースのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ce41-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="9ce41-129">カスタム フォームを作成するためにすべての MAPI フォームのインターフェイスを実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9ce41-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="9ce41-130">フォーム自体は、 **IPersistMessage**、 **IMAPIForm**を実装し、インターフェイスを**IMAPIFormAdviseSink**ことのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="9ce41-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="9ce41-131">また、それは**IMAPIFormFactory**と**IMAPIFormInfo**を実装することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9ce41-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="9ce41-132">**IMAPIFormFactory**は、OLE に準拠するために便利ですし、 **IMAPIFormInfo**は、フォームの使用方法を適切に設計されたクライアント アプリケーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9ce41-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9ce41-133">**IMAPIFormAdviseSink**は、厳密に言うと、省略可能なインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="9ce41-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="9ce41-134">ただし、フォーム サーバーに実装することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9ce41-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="9ce41-135">このインターフェイスは、メッセージング クライアントと、フォームのサーバーとの間の効率的な相互作用に重要な特にいくつかのメッセージが、フォームのサーバーのメッセージ クラスの処理中にします。</span><span class="sxs-lookup"><span data-stu-id="9ce41-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ce41-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ce41-136">See also</span></span>



[<span data-ttu-id="9ce41-137">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="9ce41-137">MAPI Forms</span></span>](mapi-forms.md)

