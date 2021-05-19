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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432521"
---
# <a name="mapi-forms-overview"></a><span data-ttu-id="1a711-103">MAPI フォームの概要</span><span class="sxs-lookup"><span data-stu-id="1a711-103">MAPI forms overview</span></span>
  
<span data-ttu-id="1a711-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a711-105">MAPI フォームは、メッセージのビューアーです。</span><span class="sxs-lookup"><span data-stu-id="1a711-105">A MAPI form is a viewer for a message.</span></span> <span data-ttu-id="1a711-106">すべてのメッセージには、ビューアーとして使用される特定のフォームを指示するメッセージ クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="1a711-106">Every message has a message class that dictates the particular form that is used as its viewer.</span></span> <span data-ttu-id="1a711-107">MAPI では、いくつかのメッセージ クラスを定義し、これらのクラスのメッセージを表示するフォームを実装しています。</span><span class="sxs-lookup"><span data-stu-id="1a711-107">MAPI defines several message classes and has implemented the forms for viewing messages of these classes.</span></span> <span data-ttu-id="1a711-108">クライアント ソフトウェア開発者は、新しいクラスを使用して作成されたメッセージを表示するために、新しいメッセージ クラスとカスタム フォームを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1a711-108">Client software developers can create new message classes and custom forms for viewing messages created by using the new classes.</span></span>
  
<span data-ttu-id="1a711-109">すべてのカスタム フォームには、Open、Create、Delete、Reply などの一連の標準メニューコマンドと、特定のフォームに固有の一連のコマンドが実装されています。 </span><span class="sxs-lookup"><span data-stu-id="1a711-109">Every custom form implements a set of standard menu commands, such as **Open**, **Create**, **Delete**, and **Reply**, and a set of commands that are specific to the particular form.</span></span> <span data-ttu-id="1a711-110">フォーム コマンドの一部は、フォームがアクティブなときにクライアント アプリケーションのユーザー インターフェイスと統合されます。その他のフォーム コマンドは、クライアント コマンドを完全に置き換える。</span><span class="sxs-lookup"><span data-stu-id="1a711-110">Some of the form commands are integrated with the user interface of the client application when the form is active; other form commands completely replace the client commands.</span></span> 
  
<span data-ttu-id="1a711-111">次の図は、フォームの使用に関係する MAPI コンポーネント間の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="1a711-111">The following illustration shows the relationship between the MAPI components involved in using forms.</span></span> 
  
<span data-ttu-id="1a711-112">**MAPI フォームのアーキテクチャ**</span><span class="sxs-lookup"><span data-stu-id="1a711-112">**MAPI form architecture**</span></span>
  
<span data-ttu-id="1a711-113">![MAPI フォーム アーキテクチャ](media/forms01.gif "MAPI フォーム アーキテクチャ")</span><span class="sxs-lookup"><span data-stu-id="1a711-113">![MAPI form architecture](media/forms01.gif "MAPI form architecture")</span></span>
  
<span data-ttu-id="1a711-114">図では、フォーム マネージャーが他の MAPI サービス プロバイダーと似た役割を果たしますが、サービス プロバイダー自体ではありません。</span><span class="sxs-lookup"><span data-stu-id="1a711-114">In the diagram, notice that the form manager plays a role that is similar to other MAPI service providers, although it is not a service provider itself.</span></span> <span data-ttu-id="1a711-115">フォーム マネージャーは、MAPI インターフェイスの一部を実装する置き換え可能な DLL です。</span><span class="sxs-lookup"><span data-stu-id="1a711-115">The form manager is a replaceable DLL that implements some of the MAPI interfaces.</span></span> <span data-ttu-id="1a711-116">開発者は独自のフォーム マネージャーを実装することができますが、ほとんどの環境では、フォーム マネージャーの複雑さのために Microsoft が提供するフォーム マネージャーを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a711-116">Although developers can implement their own form manager, most environments will use the form manager provided by Microsoft due to the form manager's complexity.</span></span>
  
<span data-ttu-id="1a711-117">次の一覧では、図のコンポーネントと他のコンポーネントとの関係について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a711-117">The following list describes the components in the diagram and their relationship to other components:</span></span>
  
- <span data-ttu-id="1a711-118">メッセージング クライアント: フォーム オブジェクトを使用できるアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="1a711-118">Messaging client: An application that can use form objects.</span></span> <span data-ttu-id="1a711-119">メッセージング クライアントは、MAPI フォーム インターフェイスを使用してフォーム マネージャーと通信し、メッセージをフォーム オブジェクトに読み込む。</span><span class="sxs-lookup"><span data-stu-id="1a711-119">The messaging client uses the MAPI form interfaces to communicate with the form manager to load messages into form objects.</span></span>
    
- <span data-ttu-id="1a711-120">MAPI フォーム インターフェイス: フォームに関連する MAPI コンポーネント間の通信に関する定義済みの標準。</span><span class="sxs-lookup"><span data-stu-id="1a711-120">MAPI form interfaces: A defined standard for communication between MAPI components that are related to forms.</span></span>
    
- <span data-ttu-id="1a711-121">フォーム マネージャー: メッセージング クライアントがフォーム ライブラリでのフォームのインストール、フォーム サーバーの読み込み、メッセージング クライアントとフォーム サーバー間の初期通信を処理するために使用する DLL。</span><span class="sxs-lookup"><span data-stu-id="1a711-121">Form manager: The DLL that messaging clients use to handle installation of forms in form libraries, loading of form servers, and initial communication between messaging clients and form servers.</span></span>
    
- <span data-ttu-id="1a711-122">フォーム ライブラリ: フォーム サーバーに関連付けられた実行可能ファイルの永続的な記憶域。</span><span class="sxs-lookup"><span data-stu-id="1a711-122">Form libraries: Permanent storage for the executable files associated with form servers.</span></span>
    
- <span data-ttu-id="1a711-123">フォーム サーバー: フォームを実装する実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="1a711-123">Form servers: Executable files that implement a form.</span></span> <span data-ttu-id="1a711-124">フォーム サーバーは、特定のメッセージを処理するフォーム オブジェクトとユーザー インターフェイスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1a711-124">Form servers create form objects and user interfaces to deal with specific messages.</span></span> <span data-ttu-id="1a711-125">この実行可能ファイルは OLE サーバーで、通常の OLE 規則に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="1a711-125">This executable is also an OLE server and adheres to the usual OLE conventions.</span></span>
    
- <span data-ttu-id="1a711-126">フォーム オブジェクト: 特定のメッセージに対応するフォーム サーバーによって作成される実行時オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="1a711-126">Form objects: Run-time objects created by form servers that correspond to specific messages.</span></span> <span data-ttu-id="1a711-127">フォーム オブジェクトは、フォーム サーバーと同じプロセス コンテキストで実行されます。</span><span class="sxs-lookup"><span data-stu-id="1a711-127">Form objects run in the same process context as their form server.</span></span>
    
<span data-ttu-id="1a711-128">MAPI フォーム コンポーネントの詳細については、「MAPI フォーム」 [を参照してください](mapi-forms.md)。</span><span class="sxs-lookup"><span data-stu-id="1a711-128">For more information about MAPI form components, see [MAPI Forms](mapi-forms.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a711-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a711-129">See also</span></span>

- [<span data-ttu-id="1a711-130">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="1a711-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

