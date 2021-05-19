---
title: MAPI フォーム サーバー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3c95f6a1d4d50dd6552c6e786d17c40da14f3f3c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419108"
---
# <a name="mapi-form-servers"></a><span data-ttu-id="d58b0-103">MAPI フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="d58b0-103">MAPI Form Servers</span></span>

  
  
<span data-ttu-id="d58b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d58b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d58b0-105">ユーザーの観点から見ると、フォームは通常、メッセージまたはデータ入力フォームのプロパティ シートで、ユーザーは構造化された情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-105">From the user's perspective, a form is usually a property sheet for a message or a data-entry form that enables users to enter structured information.</span></span> <span data-ttu-id="d58b0-106">ただし、メッセージ クラスに関連付けられている任意のユーザー インターフェイスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-106">However, it can be any user interface that is associated with a message class.</span></span> <span data-ttu-id="d58b0-107">プログラマの観点から見て、フォームは次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-107">From a programmer's point of view, a form consists of:</span></span>
  
- <span data-ttu-id="d58b0-108">独自のメッセージ クラスと OLE 識別子を持つ MAPI メッセージの種類。</span><span class="sxs-lookup"><span data-stu-id="d58b0-108">A type of MAPI message with its own message class and OLE identifier.</span></span>
    
- <span data-ttu-id="d58b0-109">フォーム サーバーを実装する実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="d58b0-109">The executable file that implements the form server.</span></span>
    
- <span data-ttu-id="d58b0-110">フォーム サーバーが使用する MAPI プロパティのコレクション (カスタムまたはそれ以外の場合)。</span><span class="sxs-lookup"><span data-stu-id="d58b0-110">A collection of MAPI properties — custom or otherwise — that the form server uses.</span></span> <span data-ttu-id="d58b0-111">これらの一部またはすべてがメッセージング クライアントで使用できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d58b0-111">Some or all of these may be available to messaging clients for use.</span></span>
    
- <span data-ttu-id="d58b0-112">フォームを記述し、フォーム マネージャーによって使用される構成ファイル。</span><span class="sxs-lookup"><span data-stu-id="d58b0-112">The configuration file that describes the form and is used by the form manager.</span></span>
    
<span data-ttu-id="d58b0-113">フォームは [IMessage オブジェクト](imessageimapiprop.md) なので、MAPI メッセージ オブジェクトと一致するプロパティと動作が示されます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-113">Because forms are [IMessage](imessageimapiprop.md) objects, they exhibit properties and behavior that is consistent with MAPI message objects.</span></span> <span data-ttu-id="d58b0-114">ただし、フォームにはカスタム プロパティ、コントロール、およびアプリケーション固有の表示レンダリングが含まれますので、フォームが使用する MAPI インターフェイスは、必要なインターフェイスの任意の種類を許可するのに十分汎用的です。</span><span class="sxs-lookup"><span data-stu-id="d58b0-114">However, because forms can have custom properties, controls, and a display rendering that is application-specific, the MAPI interfaces that forms use are generic enough to permit any sort of interface that is needed.</span></span> <span data-ttu-id="d58b0-115">フォームの実際の定義はフォーム ライブラリに格納されます。このセクションで後で説明します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-115">The actual definition of a form is stored in a form library, which is discussed later in this section.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d58b0-116">より正確に言えば、すべてのメッセージは MAPI フォームのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="d58b0-116">More accurately, all messages are instances of MAPI forms.</span></span> <span data-ttu-id="d58b0-117">ただし、一般的な電子メール メッセージを作成および読み取るフォームは最も一般的に使用されるフォームであるから、通常はカスタム フォームをメッセージの特別なケースと考える方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="d58b0-117">However, it is usually easier to think of custom forms as special cases of messages, since forms for composing and reading typical email messages are the most commonly used forms.</span></span> <span data-ttu-id="d58b0-118">すべてのメッセージが実際にはフォームだけであるという事実は、MAPI システム内の他のメッセージと同じ状態のカスタム フォームを提供します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-118">The fact that all messages are really just forms gives custom forms the same status as any other message in the MAPI system.</span></span> 
  
<span data-ttu-id="d58b0-119">すべてのフォームには一連のプロパティがあります。その一部はフォームのユーザー インターフェイスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-119">Every form has a set of properties, some of which are visible in the form's user interface.</span></span> <span data-ttu-id="d58b0-120">通常、プロパティはフォームのユーザー インターフェイスのフィールドに一致します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-120">Usually, properties are matched to fields in the form's user interface.</span></span> <span data-ttu-id="d58b0-121">たとえば、発注書フォームには、[アイテム]、[説明]、[価格]、[税金]、および [小計] というフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-121">For example, a purchase order form might have the fields Item, Description, Price, Tax, and Subtotal.</span></span> <span data-ttu-id="d58b0-122">これらのフィールドは、単に同じ名前のフォーム プロパティを視覚的にレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="d58b0-122">These fields are simply visual renderings of form properties of the same names.</span></span> <span data-ttu-id="d58b0-123">クライアントは、MAPI フォーム マネージャーによって実装される [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) メソッドを使用して、特定のメッセージ クラスでサポートされるプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-123">Clients ascertain which properties are supported by a particular message class through the [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) method, which is implemented by the MAPI form manager.</span></span> 
  
<span data-ttu-id="d58b0-124">基本的なメッセージと同様に、MAPI フォームには、送信者、目的の受信者、メッセージの送信時など、すべての標準メッセージ プロパティを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-124">Like basic messages, MAPI forms can contain all the standard message properties such as the sender, the intended recipient, and when the message was sent.</span></span> <span data-ttu-id="d58b0-125">フォームには、フォームに固有の任意の数のカスタム プロパティを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-125">Forms can also contain any number of custom properties that are specific to the form.</span></span> <span data-ttu-id="d58b0-126">たとえば、"Bug Report" フォームには、バグの種類、バグの重大度、製品バージョンのカスタム プロパティが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d58b0-126">For example a "Bug Report" form might contain custom properties for Bug Type, Bug Severity, and Product Version.</span></span>
  
<span data-ttu-id="d58b0-127">フォームを作成するには、フォーム サーバーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d58b0-127">To create a form you must implement a form server.</span></span> <span data-ttu-id="d58b0-128">フォーム サーバーは、メッセージング クライアントがフォーム サーバーでサポートされている種類のメッセージを表示する必要がある場合に読み込まれる実行可能ファイルです。</span><span class="sxs-lookup"><span data-stu-id="d58b0-128">The form server is the executable file that is loaded when a messaging client needs to display a message that is the type supported by the form server.</span></span> <span data-ttu-id="d58b0-129">フォーム サーバーは、特定のメッセージを表示し、それらのメッセージとのユーザー操作を処理するために必要に応じてフォーム オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-129">The form server in turn creates form objects as necessary to display specific messages and handle user interactions with those messages.</span></span>
  
<span data-ttu-id="d58b0-130">すべてのフォーム サーバーには、構成ファイルが関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="d58b0-130">Every form server has a configuration file associated with it.</span></span> <span data-ttu-id="d58b0-131">このファイルには、フォーム マネージャーの利点を得るフォーム サーバーについて説明する情報が含まれている。</span><span class="sxs-lookup"><span data-stu-id="d58b0-131">This file contains information that describes the form server for the benefit of the form manager.</span></span> <span data-ttu-id="d58b0-132">フォーム マネージャーは、フォーム サーバーをフォーム ライブラリにインストールするときにこの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-132">The form manager uses this information when installing the form server into a form library.</span></span>
  
<span data-ttu-id="d58b0-133">フォームのパーツの作成の詳細については、「MAPI フォーム サーバーの [開発」を参照してください](developing-mapi-form-servers.md)。</span><span class="sxs-lookup"><span data-stu-id="d58b0-133">For details on creating the parts of a form, see [Developing MAPI Form Servers](developing-mapi-form-servers.md).</span></span>
  
<span data-ttu-id="d58b0-134">フォーム サーバーは、コンポーネント オブジェクト モデル (COM) に従います。</span><span class="sxs-lookup"><span data-stu-id="d58b0-134">Form servers adhere to the Component Object Model (COM).</span></span> <span data-ttu-id="d58b0-135">フォーム サーバーは、インプロック サーバーとしてではなく、スタンドアロンの実行可能ファイルとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="d58b0-135">Form servers run as standalone executables, not as in-proc servers.</span></span> <span data-ttu-id="d58b0-136">詳細については、SDK の「COM および ActiveX オブジェクト サービス」セクションWindowsしてください。</span><span class="sxs-lookup"><span data-stu-id="d58b0-136">For more information, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
<span data-ttu-id="d58b0-137">一意のクラス識別子 (CLSID) は、各フォーム サーバーを識別します。</span><span class="sxs-lookup"><span data-stu-id="d58b0-137">A unique class identifier (CLSID) identifies each form server.</span></span> <span data-ttu-id="d58b0-138">クラス識別子とそのメッセージ クラスの間には、常に 1 対 1 のマッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="d58b0-138">There is always a one-to-one mapping between a class identifier and its message class.</span></span> <span data-ttu-id="d58b0-139">ただし、フォーム サーバーが 1 つのメッセージ クラスのメッセージのみを処理できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="d58b0-139">This does not mean, however, that a form server can only work with messages of one message class.</span></span> <span data-ttu-id="d58b0-140">特定のクラスのメッセージを処理するフォーム サーバーがない場合、使用するフォーム マネージャーは、メッセージ クラス階層の上位にあるメッセージ クラスのフォーム サーバーを検索する必要があります。SDK に付属する既定のフォーム マネージャー Windowsこれを行います。</span><span class="sxs-lookup"><span data-stu-id="d58b0-140">If no form server is available to service a message of a particular class, the form manager being used should attempt to find a form server for a message class higher in the message class hierarchy; the default form manager supplied with the Windows SDK does this.</span></span> <span data-ttu-id="d58b0-141">このようなフォーム サーバーは、メッセージのプロパティ (スーパークラスでサポートされているプロパティ) のサブセットのみをレンダリングできる可能性がありますが、何もないよりも優れたものになります。</span><span class="sxs-lookup"><span data-stu-id="d58b0-141">Such a form server will probably be able to render only a subset of the message's properties (the ones supported by the superclass), but it will be better than nothing.</span></span> <span data-ttu-id="d58b0-142">一致するフォーム サーバーが見つからない場合の処理は、使用するフォーム マネージャーに固有の実装の詳細です。この場合、既定のフォーム マネージャーはメッセージを開かれません。</span><span class="sxs-lookup"><span data-stu-id="d58b0-142">What happens when no matching form server is found at all is an implementation detail specific to the form manager being used; the default form manager does not open messages when this happens.</span></span>
  
<span data-ttu-id="d58b0-143">詳細については、「MAPI メッセージ [クラス」を参照してください](mapi-message-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="d58b0-143">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d58b0-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="d58b0-144">See also</span></span>



[<span data-ttu-id="d58b0-145">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="d58b0-145">MAPI Forms</span></span>](mapi-forms.md)

