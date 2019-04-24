---
title: MAPI フォームの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351514"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="da08c-103">MAPI フォームの概要</span><span class="sxs-lookup"><span data-stu-id="da08c-103">MAPI forms overview</span></span>
  
<span data-ttu-id="da08c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da08c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da08c-105">MAPI フォームは、メッセージのビューアーです。</span><span class="sxs-lookup"><span data-stu-id="da08c-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="da08c-106">すべてのメッセージには、その閲覧者として使用される特定のフォームを決定するメッセージクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="da08c-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="da08c-107">MAPI は、複数のメッセージクラスを定義し、これらのクラスのメッセージを表示するためのフォームを実装しています。</span><span class="sxs-lookup"><span data-stu-id="da08c-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="da08c-108">クライアントソフトウェア開発者は、新しいメッセージクラスと、新しいクラスを使用して作成されたメッセージを表示するためのカスタムフォームを作成できます。</span><span class="sxs-lookup"><span data-stu-id="da08c-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="da08c-109">すべてのカスタムフォームは、 **Open**、 **Create**、 **Delete**、 **Reply**などの標準メニューコマンドのセットと、特定のフォームに固有のコマンドのセットを実装します。</span><span class="sxs-lookup"><span data-stu-id="da08c-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="da08c-110">フォームコマンドの一部は、フォームがアクティブなときにクライアントアプリケーションのユーザーインターフェイスと統合されています。クライアントコマンドは、他のフォームコマンドによって完全に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="da08c-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="da08c-111">次の図は、フォームの使用に関連する MAPI コンポーネント間の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="da08c-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="da08c-112">**MAPI フォームのアーキテクチャ**</span><span class="sxs-lookup"><span data-stu-id="da08c-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="da08c-113">![MAPI フォームのアーキテクチャ](media/forms01.gif "MAPI フォームのアーキテクチャ")</span><span class="sxs-lookup"><span data-stu-id="da08c-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="da08c-114">図では、フォームマネージャーが他の MAPI サービスプロバイダーに似た役割を果たすことに注意してください。ただし、これはサービスプロバイダーではありません。</span><span class="sxs-lookup"><span data-stu-id="da08c-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="da08c-115">フォームマネージャーは、MAPI インターフェイスの一部を実装する、置き換え可能な DLL です。</span><span class="sxs-lookup"><span data-stu-id="da08c-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="da08c-116">開発者は独自のフォームマネージャーを実装できますが、ほとんどの環境では、フォームマネージャーの複雑さにより、Microsoft が提供するフォームマネージャーを使用します。</span><span class="sxs-lookup"><span data-stu-id="da08c-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="da08c-117">次の一覧では、ダイアグラム内のコンポーネントと、それらのコンポーネントとの関係について説明します。</span><span class="sxs-lookup"><span data-stu-id="da08c-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="da08c-118">メッセージングクライアント: form オブジェクトを使用できるアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="da08c-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="da08c-119">メッセージングクライアントは MAPI フォームインターフェイスを使用してフォームマネージャーと通信し、メッセージをフォームオブジェクトに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="da08c-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="da08c-120">mapi フォームインターフェイス: フォームに関連する mapi コンポーネント間で通信を行うために定義された標準です。</span><span class="sxs-lookup"><span data-stu-id="da08c-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="da08c-121">フォームマネージャー: メッセージングクライアントがフォームライブラリへのフォームのインストール、フォームサーバーの読み込み、およびメッセージングクライアントとフォームサーバー間の初期通信を処理するために使用する DLL。</span><span class="sxs-lookup"><span data-stu-id="da08c-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="da08c-122">フォームライブラリ: フォームサーバーに関連付けられている実行可能ファイルの永続的な保存場所。</span><span class="sxs-lookup"><span data-stu-id="da08c-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="da08c-123">フォームサーバー: フォームを実装する実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="da08c-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="da08c-124">フォームサーバーは、特定のメッセージを処理するフォームオブジェクトとユーザーインターフェイスを作成します。</span><span class="sxs-lookup"><span data-stu-id="da08c-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="da08c-125">この実行可能ファイルは ole サーバーでもあり、通常の ole の規則に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="da08c-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="da08c-126">フォームオブジェクト: フォームサーバーによって作成され、特定のメッセージに対応する実行時オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="da08c-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="da08c-127">form オブジェクトは、フォームサーバーと同じプロセスコンテキスト内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="da08c-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="da08c-128">mapi フォームコンポーネントの詳細については、「 [mapi フォーム](mapi-forms.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da08c-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da08c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="da08c-129">See also</span></span>

- [<span data-ttu-id="da08c-130">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="da08c-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

