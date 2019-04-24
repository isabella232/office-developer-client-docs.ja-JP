---
title: メッセージクラスの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285259"
---
# <a name="choosing-a-message-class"></a><span data-ttu-id="678d0-103">メッセージクラスの選択</span><span class="sxs-lookup"><span data-stu-id="678d0-103">Choosing a Message Class</span></span>

  
  
<span data-ttu-id="678d0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="678d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="678d0-105">「 [MAPI メッセージクラス](mapi-message-classes.md)」で説明されているように、メッセージクラスは、カスタムメッセージの種類とフォームサーバーの間の関係を確立する上で重要です。</span><span class="sxs-lookup"><span data-stu-id="678d0-105">As described in [MAPI Message Classes](mapi-message-classes.md), message classes are important for establishing the relationship between types of custom messages and, by extension, between form servers themselves.</span></span> <span data-ttu-id="678d0-106">さいわい、メッセージクラスの文字列を選択するのは非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="678d0-106">Fortunately, choosing a message class string is fairly simple.</span></span> <span data-ttu-id="678d0-107">メッセージクラスのメッセージクラスの文字列は任意の文字列ですが、次の規則を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-107">The message class string of a message class is an arbitrary string, but it should use the following conventions:</span></span>
  
- <span data-ttu-id="678d0-108">文字列は、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティのドキュメントで説明されているすべての規則を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-108">The string should satisfy all the conventions described in the documentation for the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span> <span data-ttu-id="678d0-109">重要なのは、文字列が ANSI 文字で構成されていて、長さが256文字未満であることです。</span><span class="sxs-lookup"><span data-stu-id="678d0-109">Importantly, the string must be composed entirely of ANSI characters and be less than 256 characters long.</span></span>
    
- <span data-ttu-id="678d0-110">フォームサーバーが既存のフォームサーバーから派生している場合、または既存のフォームサーバーの拡張機能である場合、メッセージクラスの文字列は、フォームの基になっているフォームサーバーのメッセージクラスの文字列にピリオドと別の単語を追加して作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-110">If your form server is derived from an existing form server or is an extension of an existing form server, your message class string should be formed by adding a period and another word to the message class string of the form server that your form is based on.</span></span> <span data-ttu-id="678d0-111">たとえば、会議を再スケジュールするためのフォームを実装し、フォームが会議をスケジュールするための既存のフォームに基づいているとします。</span><span class="sxs-lookup"><span data-stu-id="678d0-111">For example, you might want to implement a form to reschedule a meeting, and your form is based on an existing form for scheduling meetings.</span></span> <span data-ttu-id="678d0-112">会議スケジュールフォームのメッセージクラスの文字列が "IPM.会議 "、メッセージクラス文字列は" IPM.会議の再スケジュール "。</span><span class="sxs-lookup"><span data-stu-id="678d0-112">If the meeting scheduling form's message class string is "IPM.Meeting", your message class string could be "IPM.Meeting.Reschedule".</span></span>
    
- <span data-ttu-id="678d0-113">フォームが既存のフォームに基づいていない場合でも、メッセージクラスの文字列は "IPM." で始まっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-113">If your form is not based on any existing form, your message class string should still begin with either the "IPM."</span></span> <span data-ttu-id="678d0-114">または "IPC."</span><span class="sxs-lookup"><span data-stu-id="678d0-114">or "IPC."</span></span> <span data-ttu-id="678d0-115">プレフィックス。フォームが個人または他のアプリケーションによって受信されることを意図しているかどうかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="678d0-115">prefix, depending on whether the form is intended to be received by a person or by another application.</span></span> <span data-ttu-id="678d0-116">"IPM."</span><span class="sxs-lookup"><span data-stu-id="678d0-116">"IPM."</span></span> <span data-ttu-id="678d0-117">ユーザーの受信トレイで通常は終了する、個人間メッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="678d0-117">designates an interpersonal message that usually ends up in a user's Inbox, and "IPC."</span></span> <span data-ttu-id="678d0-118">通常、ユーザーの受信トレイに配信されないプロセス間通信メッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="678d0-118">designates an interprocess communication message that is not typically delivered to a user's Inbox.</span></span>
    
- <span data-ttu-id="678d0-119">メッセージクラスが人間に判読可能であることを意図している場合、メッセージクラスの文字列は "IPM." で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-119">If your message class is intended to be human-readable, the message class string should start with "IPM."</span></span> <span data-ttu-id="678d0-120">通常、メッセージクラスは、プレーンテキスト、HTML、またはリッチテキスト形式 (RTF) のデータを含むプロパティを使用している場合は、人間が判読可能であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="678d0-120">A message class is generally considered human-readable if it uses any properties that contain plain text, HTML, or Rich Text Format (RTF) data.</span></span> <span data-ttu-id="678d0-121">フォームで**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティを使用している場合は、ほとんどの場合、"IPM." を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-121">If your form uses the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, it should almost certainly use an "IPM."</span></span> <span data-ttu-id="678d0-122">メッセージクラスの文字列。</span><span class="sxs-lookup"><span data-stu-id="678d0-122">message class string.</span></span> <span data-ttu-id="678d0-123">たとえば、発注書用のフォームを実装していて、組織でその注文書が上司に承認されることを要求している場合、メッセージクラスの文字列は "IPM.Purchase_Order "。</span><span class="sxs-lookup"><span data-stu-id="678d0-123">For example, if you are implementing a form for purchase orders, and your organization requires that purchase orders be approved by a manager, your message class string could be "IPM.Purchase_Order".</span></span> <span data-ttu-id="678d0-124">一般に、パブリックフォルダーまたはパブリックフォルダーアプリケーションで使用するように設計されているフォームは、人物の電子メールアドレスに実際にアドレス指定されていない場合でも、ユーザーによって読み取られるため、個人外と見なされます。</span><span class="sxs-lookup"><span data-stu-id="678d0-124">Forms that are designed for use with public folders or public folder applications are typically considered to be interpersonal because they are read by people even though they are not actually addressed to any person's email address.</span></span> <span data-ttu-id="678d0-125">パブリックフォルダーのメッセージクラスの一般的なプレフィックスは、"IPM.Post "。</span><span class="sxs-lookup"><span data-stu-id="678d0-125">The typical prefix for public folder message classes is "IPM.Post".</span></span> 
    
- <span data-ttu-id="678d0-126">メッセージクラスが、ユーザーではなく、別のアプリケーションによって受信されることを意図している場合、メッセージクラスの文字列は "IPC." で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-126">If your message class is intended to be received by another application instead of by a person, the message class string should start with "IPC."</span></span> <span data-ttu-id="678d0-127">たとえば、ユーザーが自動的にメーリングリストを購読できるようにするフォームを実装する場合、メッセージクラスの文字列は "IPC" にすることができます。Subscribe "。</span><span class="sxs-lookup"><span data-stu-id="678d0-127">For example, if you are implementing a form that enables people to automatically subscribe to mailing lists, your message class string could be "IPC.Subscribe".</span></span>
    
- <span data-ttu-id="678d0-128">メッセージクラスの文字列の末尾にピリオドを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="678d0-128">Your message class string should never end with a period.</span></span>
    
<span data-ttu-id="678d0-129">メッセージクラスの文字列は、次のように、 **messageclass**エントリのフォーム構成ファイルの **[Description]** セクションに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-129">The message class string should be put in the **[Description]** section of the form configuration file, in the **MessageClass** entry, similar to the following:</span></span> 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
<span data-ttu-id="678d0-130">適切なメッセージクラスの文字列を選択したら、その文字列のクラス識別子を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-130">After you have chosen an appropriate message class string, you should generate a class identifier for it.</span></span> <span data-ttu-id="678d0-131">クラス識別子は、Visual Studio に含まれる**Create GUID**コマンドを使用して生成できます。</span><span class="sxs-lookup"><span data-stu-id="678d0-131">Class identifiers can be generated with the **Create GUID** command that is included in Visual Studio.</span></span> <span data-ttu-id="678d0-132">クラス識別子は、次のように、フォーム構成ファイルの**CLSID**エントリおよび**messageclass**エントリに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-132">The class identifier must be put in the form configuration file's **CLSID** entry, along with the **MessageClass** entry, similar to the following:</span></span> 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
<span data-ttu-id="678d0-133">もちろん、クラス識別子はほぼ確実に異なるものです。</span><span class="sxs-lookup"><span data-stu-id="678d0-133">Your class identifier will almost certainly be different, of course.</span></span> <span data-ttu-id="678d0-134">詳細については、「[フォーム構成ファイルを作成](creating-a-form-configuration-file.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="678d0-134">For more information, see [Creating a Form Configuration File](creating-a-form-configuration-file.md).</span></span>
  
<span data-ttu-id="678d0-135">ユーザーのコンピューターにフォームがインストールされている場合、インストールプロセス (セットアッププログラムであるかどうかにかかわらず) は、クラス識別子のレジストリの \*\*HKEY_CLASSES_ROOT\CLSID\* \*セクションにレジストリエントリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-135">When the form is installed on a user's computer, your installation process — whether it is a setup program or something else — must make a registry entry in the \**HKEY_CLASSES_ROOT\CLSID\** section of the registry for the class identifier.</span></span> <span data-ttu-id="678d0-136">このエントリは、メッセージクラスの文字列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="678d0-136">This entry must be set to the message class string.</span></span> <span data-ttu-id="678d0-137">たとえば、上記のクラス識別子の例については、次のようなレジストリエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="678d0-137">For example, you would create a registry entry similar to the following for the example class identifier above:</span></span> 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
<span data-ttu-id="678d0-138">詳細については、「[ライブラリへのフォームのインストール](installing-a-form-into-a-library.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="678d0-138">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="678d0-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="678d0-139">See also</span></span>



[<span data-ttu-id="678d0-140">MAPI フォームサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="678d0-140">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

