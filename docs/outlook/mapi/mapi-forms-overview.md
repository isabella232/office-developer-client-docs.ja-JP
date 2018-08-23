---
title: MAPI フォームの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 91bc0641723a92d8dc86bf3d1037d8e9936930ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801378"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="bf032-103">MAPI フォームの概要</span><span class="sxs-lookup"><span data-stu-id="bf032-103">MAPI forms overview</span></span>
  
<span data-ttu-id="bf032-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf032-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf032-105">MAPI フォームは、メッセージ ビューアーです。</span><span class="sxs-lookup"><span data-stu-id="bf032-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="bf032-106">すべてのメッセージには、そのビューアーとして使用されている特定のフォームを決定するメッセージ クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="bf032-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="bf032-107">MAPI では、いくつかのメッセージ クラスを定義し、これらのクラスのメッセージを表示するためのフォームを実装しました。</span><span class="sxs-lookup"><span data-stu-id="bf032-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="bf032-108">クライアント ソフトウェアの開発者には、メッセージの新しいクラスと新しいクラスを使用して作成されたメッセージを表示するためのカスタム フォームを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bf032-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="bf032-109">すべてのユーザー設定フォームは、**開く**、**作成**、**削除**、および**返信**などの標準のメニュー コマンドのセットとは、特定のフォームに固有のコマンドのセットを実装します。</span><span class="sxs-lookup"><span data-stu-id="bf032-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="bf032-110">フォームのコマンドの一部と統合されてクライアント アプリケーションのユーザー インターフェイスのフォームがアクティブになったときその他のフォームのコマンドは、クライアントのコマンドを完全に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="bf032-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="bf032-111">フォームの使用に関連する MAPI コンポーネント間の関係を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="bf032-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="bf032-112">**MAPI フォームのアーキテクチャ**</span><span class="sxs-lookup"><span data-stu-id="bf032-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="bf032-113">![MAPI フォームのアーキテクチャ](media/forms01.gif "MAPI フォームのアーキテクチャ")</span><span class="sxs-lookup"><span data-stu-id="bf032-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="bf032-114">図で、フォーム マネージャーがサービス ・ プロバイダー自体ではありませんがその他の MAPI サービス プロバイダーでは、次のような役割を果たすことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="bf032-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="bf032-115">フォーム マネージャーは、一部の MAPI インターフェイスを実装している交換可能な DLL です。</span><span class="sxs-lookup"><span data-stu-id="bf032-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="bf032-116">開発者が独自のフォーム マネージャーを実装できますが、ほとんどの環境はフォーム マネージャーの複雑さのため、Microsoft によって提供されるフォーム マネージャーを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf032-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="bf032-117">次の一覧には、コンポーネント図とその他のコンポーネントとの関係について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf032-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="bf032-118">メッセージング クライアント: フォーム オブジェクトを使用するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="bf032-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="bf032-119">メッセージング クライアントでは、フォーム オブジェクトにメッセージをロードするのには、フォームのマネージャーとの通信に MAPI フォームのインタ フェースを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf032-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="bf032-120">MAPI フォームのインタ フェース: 定義済みの標準フォームに関連する MAPI コンポーネント間の通信します。</span><span class="sxs-lookup"><span data-stu-id="bf032-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="bf032-121">マネージャーのフォーム: フォーム ライブラリ内のフォームのインストール、フォームのサーバーとメッセージング クライアントとサーバーのフォーム間の初期通信の読み込みを処理するメッセージング クライアントを使用する DLL です。</span><span class="sxs-lookup"><span data-stu-id="bf032-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="bf032-122">フォーム ライブラリ: フォームのサーバーに関連付けられている実行可能ファイルを恒久的に保存します。</span><span class="sxs-lookup"><span data-stu-id="bf032-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="bf032-123">サーバーのフォーム: フォームを実装する実行可能ファイルです。</span><span class="sxs-lookup"><span data-stu-id="bf032-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="bf032-124">フォームのサーバーでは、フォームのオブジェクトと特定のメッセージに対処するためのユーザー インターフェイスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bf032-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="bf032-125">この実行可能ファイルが OLE サーバーにも、OLE の通常の規則に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="bf032-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="bf032-126">オブジェクトを形成する: 特定のメッセージに対応するフォームのサーバーによって作成された実行時のオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="bf032-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="bf032-127">フォーム オブジェクトは、フォーム サーバーとして、同じプロセス コンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="bf032-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="bf032-128">MAPI フォーム コンポーネントの詳細については、 [MAPI フォーム](mapi-forms.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf032-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf032-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf032-129">See also</span></span>

- [<span data-ttu-id="bf032-130">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="bf032-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

