---
title: メッセージ クラスの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c3b486838c6ce2d7fc38d950a4de6f4589767073
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574238"
---
# <a name="choosing-a-message-class"></a><span data-ttu-id="bea61-103">メッセージ クラスの選択</span><span class="sxs-lookup"><span data-stu-id="bea61-103">Choosing a Message Class</span></span>

  
  
<span data-ttu-id="bea61-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bea61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bea61-105">[MAPI メッセージ クラス](mapi-message-classes.md)で説明したとおり、メッセージ クラスは、カスタム メッセージのさらに、拡張して、フォーム サーバー自体の間での型の間の関係を確立するために重要です。</span><span class="sxs-lookup"><span data-stu-id="bea61-105">As described in [MAPI Message Classes](mapi-message-classes.md), message classes are important for establishing the relationship between types of custom messages and, by extension, between form servers themselves.</span></span> <span data-ttu-id="bea61-106">幸いなことに、メッセージ クラスの文字列を選択することは非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="bea61-106">Fortunately, choosing a message class string is fairly simple.</span></span> <span data-ttu-id="bea61-107">メッセージ クラスのメッセージ クラスの文字列は、任意の文字列ですが、次の表記規則を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-107">The message class string of a message class is an arbitrary string, but it should use the following conventions:</span></span>
  
- <span data-ttu-id="bea61-108">文字列は、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティのドキュメントに記載されているすべての規則を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-108">The string should satisfy all the conventions described in the documentation for the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span> <span data-ttu-id="bea61-109">重要なは、文字列は ANSI 文字のみで構成して、半角 256 文字未満にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-109">Importantly, the string must be composed entirely of ANSI characters and be less than 256 characters long.</span></span>
    
- <span data-ttu-id="bea61-110">フォーム サーバーは、フォームの既存のサーバーから派生したまたはフォームの既存のサーバーの拡張機能では、サーバーに基づいて、フォームをフォームのメッセージ クラスの文字列にピリオドと別の単語を追加することによって、メッセージ クラスの文字列を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-110">If your form server is derived from an existing form server or is an extension of an existing form server, your message class string should be formed by adding a period and another word to the message class string of the form server that your form is based on.</span></span> <span data-ttu-id="bea61-111">など、会議のスケジュールを変更するフォームを実装することもできますし、会議をスケジュールするための既存のフォームに基づいて、フォームです。</span><span class="sxs-lookup"><span data-stu-id="bea61-111">For example, you might want to implement a form to reschedule a meeting, and your form is based on an existing form for scheduling meetings.</span></span> <span data-ttu-id="bea61-112">会議のスケジュール設定のフォームのメッセージ クラスの文字列は"IPM. 場合、会議"で、メッセージ クラスの文字列があります"IPM.Meeting.Reschedule"です。</span><span class="sxs-lookup"><span data-stu-id="bea61-112">If the meeting scheduling form's message class string is "IPM.Meeting", your message class string could be "IPM.Meeting.Reschedule".</span></span>
    
- <span data-ttu-id="bea61-113">フォームが基づいていない場合、既存のフォームに、メッセージのクラスの文字列も、まずいずれか、"IPM."</span><span class="sxs-lookup"><span data-stu-id="bea61-113">If your form is not based on any existing form, your message class string should still begin with either the "IPM."</span></span> <span data-ttu-id="bea61-114">または"IPC"にします。</span><span class="sxs-lookup"><span data-stu-id="bea61-114">or "IPC."</span></span> <span data-ttu-id="bea61-115">プレフィックス、フォームは、ユーザーまたは別のアプリケーションによって受信されるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="bea61-115">prefix, depending on whether the form is intended to be received by a person or by another application.</span></span> <span data-ttu-id="bea61-116">"IPM."</span><span class="sxs-lookup"><span data-stu-id="bea61-116">"IPM."</span></span> <span data-ttu-id="bea61-117">通常ユーザーの受信トレイ、および"IPC。"内に格納される個人間のメッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="bea61-117">designates an interpersonal message that usually ends up in a user's Inbox, and "IPC."</span></span> <span data-ttu-id="bea61-118">通常はユーザーの受信トレイには配信されませんが、プロセス間通信メッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="bea61-118">designates an interprocess communication message that is not typically delivered to a user's Inbox.</span></span>
    
- <span data-ttu-id="bea61-119">メッセージ クラスの文字列が"IPM."で開始する必要がある場合は、メッセージ クラスは、ユーザーが判読できる、</span><span class="sxs-lookup"><span data-stu-id="bea61-119">If your message class is intended to be human-readable, the message class string should start with "IPM."</span></span> <span data-ttu-id="bea61-120">メッセージ クラスは、通常と見なされる人間が判読できるテキスト形式、HTML が含まれている任意のプロパティを使用する場合、またはリッチ テキスト形式 (RTF) データ。</span><span class="sxs-lookup"><span data-stu-id="bea61-120">A message class is generally considered human-readable if it uses any properties that contain plain text, HTML, or Rich Text Format (RTF) data.</span></span> <span data-ttu-id="bea61-121">フォームは、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティを使用している場合は、"IPM."をほぼ確実に使用してください。</span><span class="sxs-lookup"><span data-stu-id="bea61-121">If your form uses the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, it should almost certainly use an "IPM."</span></span> <span data-ttu-id="bea61-122">メッセージ クラスの文字列です。</span><span class="sxs-lookup"><span data-stu-id="bea61-122">message class string.</span></span> <span data-ttu-id="bea61-123">たとえば、発注書のフォームを実装すると、管理者による、発注書を承認することを必要とする組織、メッセージ クラス文字列可能性があります"IPM.Purchase_Order"です。</span><span class="sxs-lookup"><span data-stu-id="bea61-123">For example, if you are implementing a form for purchase orders, and your organization requires that purchase orders be approved by a manager, your message class string could be "IPM.Purchase_Order".</span></span> <span data-ttu-id="bea61-124">パブリック フォルダー用に作成されたフォームを使用して、またはパブリック フォルダー アプリケーション通常と見なされる対人関係の人の電子メール アドレスに実際には対応できない場合でも人によって読み取られるためです。</span><span class="sxs-lookup"><span data-stu-id="bea61-124">Forms that are designed for use with public folders or public folder applications are typically considered to be interpersonal because they are read by people even though they are not actually addressed to any person's email address.</span></span> <span data-ttu-id="bea61-125">パブリック フォルダーのメッセージ クラスの代表的なプリフィックスは、"IPM.投稿」です。</span><span class="sxs-lookup"><span data-stu-id="bea61-125">The typical prefix for public folder message classes is "IPM.Post".</span></span> 
    
- <span data-ttu-id="bea61-126">メッセージ クラスの文字列が"IPC"で開始する必要がある場合は、メッセージ クラスの代わりに別のアプリケーションで受信する人が、</span><span class="sxs-lookup"><span data-stu-id="bea61-126">If your message class is intended to be received by another application instead of by a person, the message class string should start with "IPC."</span></span> <span data-ttu-id="bea61-127">たとえば、自動的にメーリング リストの購読を可能にするフォームを実装する場合、メッセージ クラスの文字列可能性があります"IPC。」を購読します。</span><span class="sxs-lookup"><span data-stu-id="bea61-127">For example, if you are implementing a form that enables people to automatically subscribe to mailing lists, your message class string could be "IPC.Subscribe".</span></span>
    
- <span data-ttu-id="bea61-128">メッセージのクラスの文字列は、ピリオドで終わる必要があることはありません。</span><span class="sxs-lookup"><span data-stu-id="bea61-128">Your message class string should never end with a period.</span></span>
    
<span data-ttu-id="bea61-129">**MessageClass**エントリでは、次のようなフォーム構成ファイルの **[説明]** セクションでは、メッセージ クラスの文字列を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-129">The message class string should be put in the **[Description]** section of the form configuration file, in the **MessageClass** entry, similar to the following:</span></span> 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
<span data-ttu-id="bea61-130">適切なメッセージ クラスの文字列を選択した後のクラス識別子を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-130">After you have chosen an appropriate message class string, you should generate a class identifier for it.</span></span> <span data-ttu-id="bea61-131">クラス識別子は、Visual Studio に含まれる**GUID の作成**] コマンドを使って生成できます。</span><span class="sxs-lookup"><span data-stu-id="bea61-131">Class identifiers can be generated with the **Create GUID** command that is included in Visual Studio.</span></span> <span data-ttu-id="bea61-132">**MessageClass**エントリでは、次のようなと、フォーム構成ファイルの**CLSID**エントリのクラス識別子を置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-132">The class identifier must be put in the form configuration file's **CLSID** entry, along with the **MessageClass** entry, similar to the following:</span></span> 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
<span data-ttu-id="bea61-133">クラス識別子は、ほぼ確実に変更されます、もちろん。</span><span class="sxs-lookup"><span data-stu-id="bea61-133">Your class identifier will almost certainly be different, of course.</span></span> <span data-ttu-id="bea61-134">詳細については、[フォーム構成ファイルを作成する](creating-a-form-configuration-file.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bea61-134">For more information, see [Creating a Form Configuration File](creating-a-form-configuration-file.md).</span></span>
  
<span data-ttu-id="bea61-135">ユーザーのコンピューターでは、インストール プロセスは、フォームがインストールされている場合、セットアップ プログラムまたは他の何かあるかどうか-のレジストリ エントリを作成する必要があります、**見つけてクリック\** クラス識別子のレジストリのセクションです。</span><span class="sxs-lookup"><span data-stu-id="bea61-135">When the form is installed on a user's computer, your installation process — whether it is a setup program or something else — must make a registry entry in the **HKEY_CLASSES_ROOT\CLSID\** section of the registry for the class identifier.</span></span> <span data-ttu-id="bea61-136">このエントリは、メッセージ クラスの文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bea61-136">This entry must be set to the message class string.</span></span> <span data-ttu-id="bea61-137">などがエントリを作成するレジストリ上の例のクラス識別子は、次のような。</span><span class="sxs-lookup"><span data-stu-id="bea61-137">For example, you would create a registry entry similar to the following for the example class identifier above:</span></span> 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
<span data-ttu-id="bea61-138">詳細については、[ライブラリにフォームをインストールする](installing-a-form-into-a-library.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bea61-138">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bea61-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="bea61-139">See also</span></span>



[<span data-ttu-id="bea61-140">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="bea61-140">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

