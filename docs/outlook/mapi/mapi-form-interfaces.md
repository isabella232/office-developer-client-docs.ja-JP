---
title: MAPI フォーム インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412346"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="6ad22-103">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6ad22-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="6ad22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ad22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ad22-105">MAPI は、フォームに関連する次のインターフェイスを定義します。</span><span class="sxs-lookup"><span data-stu-id="6ad22-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="6ad22-106">**インターフェイス名**</span><span class="sxs-lookup"><span data-stu-id="6ad22-106">**Interface name**</span></span>|<span data-ttu-id="6ad22-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ad22-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ad22-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="6ad22-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="6ad22-109">フォーム オブジェクトを操作し、フォーム オブジェクト コマンドを処理します。</span><span class="sxs-lookup"><span data-stu-id="6ad22-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6ad22-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="6ad22-111">フォーム オブジェクトが次のメッセージを処理できるかどうかを判断し、フォーム オブジェクトの次または前の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="6ad22-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="6ad22-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="6ad22-113">特定のフォーム コンテナーに対するフォーム サーバーのインストール、アンインストール、および解決をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ad22-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="6ad22-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="6ad22-115">構成可能な実行時フォーム サーバーの使用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ad22-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="6ad22-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="6ad22-117">クライアント アプリケーションがメッセージ クラスに固有のプロパティを操作できます。</span><span class="sxs-lookup"><span data-stu-id="6ad22-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="6ad22-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="6ad22-119">クライアント アプリケーションがフォーム サーバーに関する情報を取得し、フォーム サーバーをアクティブ化し、メッセージング システムにフォーム サーバーをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="6ad22-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="6ad22-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="6ad22-121">フォーム オブジェクトに関連付けられたメッセージを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6ad22-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6ad22-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="6ad22-123">フォーム オブジェクトでイベントが発生したとクライアント アプリケーションに通知します。</span><span class="sxs-lookup"><span data-stu-id="6ad22-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="6ad22-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="6ad22-125">フォーム オブジェクトの [次へ]、[前へ]、および [削除] のコマンドに応答するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6ad22-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="6ad22-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="6ad22-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="6ad22-127">メッセージ ストレージ間のフォーム オブジェクトの保存、初期化、読み込みに使用されます。</span><span class="sxs-lookup"><span data-stu-id="6ad22-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="6ad22-128">MAPI フォーム インターフェイスのメソッドの詳細については、これらのインターフェイスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ad22-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="6ad22-129">カスタム フォームを作成するには、すべての MAPI フォーム インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ad22-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="6ad22-130">フォーム自体は **、IPersistMessage、IMAPIForm、\*\*\*\*および IMAPIFormAdviseSink** インターフェイスを実装する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="6ad22-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="6ad22-131">さらに **、IMAPIFormFactory と IMAPIFormInfo** を実装 **するのも良い考えです**。</span><span class="sxs-lookup"><span data-stu-id="6ad22-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="6ad22-132">**IMAPIFormFactory は** OLE コンプライアンスに役立ち **、IMAPIFormInfo** を使用すると、適切に記述されたクライアント アプリケーションでフォームをより有効に利用できます。</span><span class="sxs-lookup"><span data-stu-id="6ad22-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6ad22-133">厳密に言えば **、IMAPIFormAdviseSink** はオプションのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="6ad22-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="6ad22-134">ただし、フォーム サーバーに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ad22-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="6ad22-135">このインターフェイスは、特にフォーム サーバーのメッセージ クラスのいくつかのメッセージが処理されている場合に、メッセージング クライアントとフォーム サーバー間の効率的なやり取りを行う上で重要です。</span><span class="sxs-lookup"><span data-stu-id="6ad22-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ad22-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ad22-136">See also</span></span>



[<span data-ttu-id="6ad22-137">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="6ad22-137">MAPI Forms</span></span>](mapi-forms.md)

