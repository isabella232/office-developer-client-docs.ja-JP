---
title: MAPI フォームインターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351542"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="3de57-103">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3de57-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="3de57-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3de57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3de57-105">MAPI は、フォームに関連する次のインターフェイスを定義します。</span><span class="sxs-lookup"><span data-stu-id="3de57-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="3de57-106">**インターフェイス名**</span><span class="sxs-lookup"><span data-stu-id="3de57-106">**Interface name**</span></span>|<span data-ttu-id="3de57-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="3de57-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3de57-108">imapiform</span><span class="sxs-lookup"><span data-stu-id="3de57-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="3de57-109">フォームオブジェクトを操作し、フォームオブジェクトのコマンドを処理します。</span><span class="sxs-lookup"><span data-stu-id="3de57-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="3de57-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3de57-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="3de57-111">form オブジェクトが次のメッセージを処理できるかどうかを調べ、form オブジェクトの次または前の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="3de57-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="3de57-112">imapiformcontainer</span><span class="sxs-lookup"><span data-stu-id="3de57-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="3de57-113">特定のフォームコンテナーに対するフォームサーバーのインストール、アンインストール、および解決をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3de57-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="3de57-114">imapiformfactory</span><span class="sxs-lookup"><span data-stu-id="3de57-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="3de57-115">構成可能な実行時フォームサーバーの使用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3de57-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="3de57-116">imapiforminfo</span><span class="sxs-lookup"><span data-stu-id="3de57-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="3de57-117">クライアントアプリケーションが、メッセージクラスに固有のプロパティを処理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3de57-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="3de57-118">imapiformmgr</span><span class="sxs-lookup"><span data-stu-id="3de57-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="3de57-119">クライアントアプリケーションがフォームサーバーに関する情報を取得し、フォームサーバーをアクティブ化して、メッセージングシステムにフォームサーバーをインストールできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3de57-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="3de57-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="3de57-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="3de57-121">フォームオブジェクトに関連付けられたメッセージを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3de57-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="3de57-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3de57-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="3de57-123">form オブジェクト内でイベントが発生したことをクライアントアプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="3de57-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="3de57-124">imapiviewcontext</span><span class="sxs-lookup"><span data-stu-id="3de57-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="3de57-125">form オブジェクト内の次、前、および削除コマンドに応答するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3de57-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="3de57-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="3de57-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="3de57-127">メッセージストレージとの間でフォームオブジェクトの保存、初期化、および読み込みを行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3de57-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="3de57-128">MAPI フォームインターフェイスのメソッドの詳細については、これらのインターフェイスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3de57-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="3de57-129">カスタムフォームを作成するために、すべての MAPI フォームインターフェイスを実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3de57-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="3de57-130">フォーム自体で必要なのは、 **IPersistMessage**、 **imapiform**、および**IMAPIFormAdviseSink**インターフェイスを実装することだけです。</span><span class="sxs-lookup"><span data-stu-id="3de57-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="3de57-131">また、 **imapiformfactory**および**imapiformfactory**を実装することもお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3de57-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="3de57-132">**imapiformfactory**は OLE のコンプライアンスに役立ち、 **imapiformfactory**を使用すると、適切に記述されたクライアントアプリケーションがフォームをより適切に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3de57-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3de57-133">厳密に言うと、 **IMAPIFormAdviseSink**はオプションのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="3de57-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="3de57-134">ただし、フォームサーバーに実装することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3de57-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="3de57-135">このインターフェイスは、メッセージングクライアントとフォームサーバー間の対話を効率的に行うために重要です。特に、フォームサーバーのメッセージクラスの複数のメッセージが処理されている場合です。</span><span class="sxs-lookup"><span data-stu-id="3de57-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3de57-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="3de57-136">See also</span></span>



[<span data-ttu-id="3de57-137">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="3de57-137">MAPI Forms</span></span>](mapi-forms.md)

