---
title: メッセージ クラスの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428054"
---
# <a name="choosing-a-message-class"></a><span data-ttu-id="16ce9-103">メッセージ クラスの選択</span><span class="sxs-lookup"><span data-stu-id="16ce9-103">Choosing a Message Class</span></span>

  
  
<span data-ttu-id="16ce9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16ce9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16ce9-105">「MAPI メッセージ [クラス」](mapi-message-classes.md)で説明したように、メッセージ クラスは、カスタム メッセージの種類と、フォーム サーバー自体の間のリレーションシップを拡張して確立するために重要です。</span><span class="sxs-lookup"><span data-stu-id="16ce9-105">As described in [MAPI Message Classes](mapi-message-classes.md), message classes are important for establishing the relationship between types of custom messages and, by extension, between form servers themselves.</span></span> <span data-ttu-id="16ce9-106">幸いなことに、メッセージ クラス文字列の選択はかなり簡単です。</span><span class="sxs-lookup"><span data-stu-id="16ce9-106">Fortunately, choosing a message class string is fairly simple.</span></span> <span data-ttu-id="16ce9-107">メッセージ クラスのメッセージ クラス文字列は任意の文字列ですが、次の規則を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-107">The message class string of a message class is an arbitrary string, but it should use the following conventions:</span></span>
  
- <span data-ttu-id="16ce9-108">文字列は、プロパティ ([PidTagMessageClass](pidtagmessageclass-canonical-property.md) **)** プロパティのドキュメントで説明PR_MESSAGE_CLASS規則をすべて満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-108">The string should satisfy all the conventions described in the documentation for the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span> <span data-ttu-id="16ce9-109">重要な点として、文字列は ANSI 文字で構成され、長さ 256 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-109">Importantly, the string must be composed entirely of ANSI characters and be less than 256 characters long.</span></span>
    
- <span data-ttu-id="16ce9-110">フォーム サーバーが既存のフォーム サーバーから派生している場合、または既存のフォーム サーバーの拡張機能である場合は、フォームの基になるフォーム サーバーのメッセージ クラス文字列にピリオドと別の単語を追加して、メッセージ クラス文字列を形成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-110">If your form server is derived from an existing form server or is an extension of an existing form server, your message class string should be formed by adding a period and another word to the message class string of the form server that your form is based on.</span></span> <span data-ttu-id="16ce9-111">たとえば、会議のスケジュールを変更するフォームを実装する場合、フォームは会議のスケジュールを設定するための既存のフォームに基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="16ce9-111">For example, you might want to implement a form to reschedule a meeting, and your form is based on an existing form for scheduling meetings.</span></span> <span data-ttu-id="16ce9-112">会議スケジュール フォームのメッセージ クラス文字列が "IPM" の場合。会議」の場合、メッセージ クラスの文字列は "IPM" になります。Meeting.Reschedule」</span><span class="sxs-lookup"><span data-stu-id="16ce9-112">If the meeting scheduling form's message class string is "IPM.Meeting", your message class string could be "IPM.Meeting.Reschedule".</span></span>
    
- <span data-ttu-id="16ce9-113">フォームが既存のフォームに基づいていない場合でも、メッセージ クラス文字列は "IPM" で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-113">If your form is not based on any existing form, your message class string should still begin with either the "IPM."</span></span> <span data-ttu-id="16ce9-114">または "IPC"</span><span class="sxs-lookup"><span data-stu-id="16ce9-114">or "IPC."</span></span> <span data-ttu-id="16ce9-115">フォームがユーザーまたは別のアプリケーションによって受信される対象かどうかに応じて、プレフィックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="16ce9-115">prefix, depending on whether the form is intended to be received by a person or by another application.</span></span> <span data-ttu-id="16ce9-116">"IPM"</span><span class="sxs-lookup"><span data-stu-id="16ce9-116">"IPM."</span></span> <span data-ttu-id="16ce9-117">通常、ユーザーの受信トレイで終わる対人メッセージと "IPC" を指定します。</span><span class="sxs-lookup"><span data-stu-id="16ce9-117">designates an interpersonal message that usually ends up in a user's Inbox, and "IPC."</span></span> <span data-ttu-id="16ce9-118">通常、ユーザーの受信トレイに配信されないプロセス間通信メッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="16ce9-118">designates an interprocess communication message that is not typically delivered to a user's Inbox.</span></span>
    
- <span data-ttu-id="16ce9-119">メッセージ クラスが人間が読み取り可能な場合、メッセージ クラス文字列は "IPM" で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-119">If your message class is intended to be human-readable, the message class string should start with "IPM."</span></span> <span data-ttu-id="16ce9-120">メッセージ クラスは、通常、テキスト形式、HTML 形式、またはリッチ テキスト形式 (RTF) データを含むプロパティを使用する場合、人間が読み取り可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="16ce9-120">A message class is generally considered human-readable if it uses any properties that contain plain text, HTML, or Rich Text Format (RTF) data.</span></span> <span data-ttu-id="16ce9-121">フォームでプロパティ ([PidTagBody](pidtagbody-canonical-property.md) **)** PR_BODY使用する場合は、ほぼ確実に "IPM" を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-121">If your form uses the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, it should almost certainly use an "IPM."</span></span> <span data-ttu-id="16ce9-122">メッセージ クラスの文字列。</span><span class="sxs-lookup"><span data-stu-id="16ce9-122">message class string.</span></span> <span data-ttu-id="16ce9-123">たとえば、発注書のフォームを実装している場合に、組織が発注書をマネージャーによって承認する必要がある場合、メッセージ クラス文字列は "IPM" になります。Purchase_Order」</span><span class="sxs-lookup"><span data-stu-id="16ce9-123">For example, if you are implementing a form for purchase orders, and your organization requires that purchase orders be approved by a manager, your message class string could be "IPM.Purchase_Order".</span></span> <span data-ttu-id="16ce9-124">パブリック フォルダーまたはパブリック フォルダー アプリケーションで使用するように設計されたフォームは、実際には任意のユーザーの電子メール アドレスにアドレス指定されていない場合でも、ユーザーが読み取るので、通常は対人的であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="16ce9-124">Forms that are designed for use with public folders or public folder applications are typically considered to be interpersonal because they are read by people even though they are not actually addressed to any person's email address.</span></span> <span data-ttu-id="16ce9-125">パブリック フォルダー メッセージ クラスの一般的なプレフィックスは"IPM" です。Post」</span><span class="sxs-lookup"><span data-stu-id="16ce9-125">The typical prefix for public folder message classes is "IPM.Post".</span></span> 
    
- <span data-ttu-id="16ce9-126">メッセージ クラスがユーザーではなく別のアプリケーションによって受信される場合、メッセージ クラス文字列は "IPC" で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-126">If your message class is intended to be received by another application instead of by a person, the message class string should start with "IPC."</span></span> <span data-ttu-id="16ce9-127">たとえば、ユーザーが自動的にメーリングリストを購読できるフォームを実装している場合、メッセージ クラス文字列は "IPC" になります。[サブスクライブ]</span><span class="sxs-lookup"><span data-stu-id="16ce9-127">For example, if you are implementing a form that enables people to automatically subscribe to mailing lists, your message class string could be "IPC.Subscribe".</span></span>
    
- <span data-ttu-id="16ce9-128">メッセージ クラスの文字列は、ピリオドで終わる必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-128">Your message class string should never end with a period.</span></span>
    
<span data-ttu-id="16ce9-129">メッセージ クラスの文字列は、次のような **MessageClass** エントリのフォーム構成ファイルの **[Description]** セクションに置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-129">The message class string should be put in the **[Description]** section of the form configuration file, in the **MessageClass** entry, similar to the following:</span></span> 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
<span data-ttu-id="16ce9-130">適切なメッセージ クラス文字列を選択したら、そのクラス識別子を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-130">After you have chosen an appropriate message class string, you should generate a class identifier for it.</span></span> <span data-ttu-id="16ce9-131">クラス識別子は、クラス識別子に含まれる **GUID** の作成コマンドを使用してVisual Studio。</span><span class="sxs-lookup"><span data-stu-id="16ce9-131">Class identifiers can be generated with the **Create GUID** command that is included in Visual Studio.</span></span> <span data-ttu-id="16ce9-132">クラス識別子は、次のような **MessageClass** エントリと共に、フォーム構成ファイルの **CLSID** エントリに入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-132">The class identifier must be put in the form configuration file's **CLSID** entry, along with the **MessageClass** entry, similar to the following:</span></span> 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
<span data-ttu-id="16ce9-133">もちろん、クラス識別子はほぼ確実に異なります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-133">Your class identifier will almost certainly be different, of course.</span></span> <span data-ttu-id="16ce9-134">詳細については、「フォーム構成ファイルの [作成」を参照してください](creating-a-form-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="16ce9-134">For more information, see [Creating a Form Configuration File](creating-a-form-configuration-file.md).</span></span>
  
<span data-ttu-id="16ce9-135">フォームがユーザーのコンピューターにインストールされている場合、セットアップ プログラムや他のプログラムに関係ないインストール プロセスでは、クラス識別子のレジストリの \**HKEY_CLASSES_ROOT\CLSID\** セクションにレジストリ エントリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-135">When the form is installed on a user's computer, your installation process — whether it is a setup program or something else — must make a registry entry in the \**HKEY_CLASSES_ROOT\CLSID\** section of the registry for the class identifier.</span></span> <span data-ttu-id="16ce9-136">このエントリは、メッセージ クラス文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ce9-136">This entry must be set to the message class string.</span></span> <span data-ttu-id="16ce9-137">たとえば、上記のクラス識別子の例では、次のようなレジストリ エントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="16ce9-137">For example, you would create a registry entry similar to the following for the example class identifier above:</span></span> 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
<span data-ttu-id="16ce9-138">詳細については、「ライブラリへの [フォームのインストール」を参照してください](installing-a-form-into-a-library.md)。</span><span class="sxs-lookup"><span data-stu-id="16ce9-138">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16ce9-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="16ce9-139">See also</span></span>



[<span data-ttu-id="16ce9-140">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="16ce9-140">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

