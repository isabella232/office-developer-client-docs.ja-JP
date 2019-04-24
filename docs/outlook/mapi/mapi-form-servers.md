---
title: MAPI フォームサーバー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3c95f6a1d4d50dd6552c6e786d17c40da14f3f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351486"
---
# <a name="mapi-form-servers"></a><span data-ttu-id="f77c9-103">MAPI フォームサーバー</span><span class="sxs-lookup"><span data-stu-id="f77c9-103">MAPI Form Servers</span></span>

  
  
<span data-ttu-id="f77c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f77c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f77c9-105">ユーザーの視点から見ると、通常、フォームは、ユーザーが構造化された情報を入力できるようにする、メッセージまたはデータ入力フォームのプロパティシートです。</span><span class="sxs-lookup"><span data-stu-id="f77c9-105">From the user's perspective, a form is usually a property sheet for a message or a data-entry form that enables users to enter structured information.</span></span> <span data-ttu-id="f77c9-106">ただし、メッセージクラスに関連付けられている任意のユーザーインターフェイスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-106">However, it can be any user interface that is associated with a message class.</span></span> <span data-ttu-id="f77c9-107">プログラマの視点から見ると、フォームは次の要素で構成されています。</span><span class="sxs-lookup"><span data-stu-id="f77c9-107">From a programmer's point of view, a form consists of:</span></span>
  
- <span data-ttu-id="f77c9-108">独自のメッセージクラスと OLE 識別子を持つ MAPI メッセージの種類。</span><span class="sxs-lookup"><span data-stu-id="f77c9-108">A type of MAPI message with its own message class and OLE identifier.</span></span>
    
- <span data-ttu-id="f77c9-109">フォームサーバーを実装する実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="f77c9-109">The executable file that implements the form server.</span></span>
    
- <span data-ttu-id="f77c9-110">フォームサーバーで使用される MAPI プロパティのコレクション (カスタムまたはそれ以外)。</span><span class="sxs-lookup"><span data-stu-id="f77c9-110">A collection of MAPI properties — custom or otherwise — that the form server uses.</span></span> <span data-ttu-id="f77c9-111">これらの一部またはすべてを、メッセージングクライアントが使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-111">Some or all of these may be available to messaging clients for use.</span></span>
    
- <span data-ttu-id="f77c9-112">フォームを説明する構成ファイル。フォームマネージャーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-112">The configuration file that describes the form and is used by the form manager.</span></span>
    
<span data-ttu-id="f77c9-113">フォームは[IMessage](imessageimapiprop.md)オブジェクトであるため、MAPI メッセージオブジェクトと一貫性のあるプロパティと動作が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-113">Because forms are [IMessage](imessageimapiprop.md) objects, they exhibit properties and behavior that is consistent with MAPI message objects.</span></span> <span data-ttu-id="f77c9-114">ただし、フォームには、カスタムプロパティ、コントロール、およびアプリケーション固有の表示レンダリングがあるため、フォームで使用される MAPI インターフェイスは汎用的なものであり、必要なインターフェイスのあらゆる種類を許可します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-114">However, because forms can have custom properties, controls, and a display rendering that is application-specific, the MAPI interfaces that forms use are generic enough to permit any sort of interface that is needed.</span></span> <span data-ttu-id="f77c9-115">フォームの実際の定義は、フォームライブラリに格納されます。これについては、このセクションで後述します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-115">The actual definition of a form is stored in a form library, which is discussed later in this section.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f77c9-116">正確には、すべてのメッセージは MAPI フォームのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="f77c9-116">More accurately, all messages are instances of MAPI forms.</span></span> <span data-ttu-id="f77c9-117">ただし、通常の電子メールメッセージを作成するためのフォームが最もよく使用されるフォームなので、ユーザー設定フォームは、通常、メッセージの特殊なケースとして考えるほうが簡単です。</span><span class="sxs-lookup"><span data-stu-id="f77c9-117">However, it is usually easier to think of custom forms as special cases of messages, since forms for composing and reading typical email messages are the most commonly used forms.</span></span> <span data-ttu-id="f77c9-118">すべてのメッセージは単にフォームであるため、カスタムフォームには MAPI システムの他のメッセージと同じ状態が与えられます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-118">The fact that all messages are really just forms gives custom forms the same status as any other message in the MAPI system.</span></span> 
  
<span data-ttu-id="f77c9-119">すべてのフォームには一連のプロパティがあり、その一部はフォームのユーザーインターフェイスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-119">Every form has a set of properties, some of which are visible in the form's user interface.</span></span> <span data-ttu-id="f77c9-120">通常、プロパティはフォームのユーザーインターフェイスのフィールドと一致します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-120">Usually, properties are matched to fields in the form's user interface.</span></span> <span data-ttu-id="f77c9-121">たとえば、発注書フォームには、フィールドアイテム、説明、価格、税金、および小計があります。</span><span class="sxs-lookup"><span data-stu-id="f77c9-121">For example, a purchase order form might have the fields Item, Description, Price, Tax, and Subtotal.</span></span> <span data-ttu-id="f77c9-122">これらのフィールドは、同じ名前のフォームプロパティを視覚的に表示するだけです。</span><span class="sxs-lookup"><span data-stu-id="f77c9-122">These fields are simply visual renderings of form properties of the same names.</span></span> <span data-ttu-id="f77c9-123">クライアントは、MAPI フォームマネージャーで実装されている[imapiforminfo:: CalcFormPropSet](imapiforminfo-calcformpropset.md)メソッドを使用して、特定のメッセージクラスでサポートされているプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-123">Clients ascertain which properties are supported by a particular message class through the [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) method, which is implemented by the MAPI form manager.</span></span> 
  
<span data-ttu-id="f77c9-124">MAPI フォームには、基本メッセージと同様に、送信者、目的の受信者、メッセージの送信日時など、すべての標準メッセージプロパティを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-124">Like basic messages, MAPI forms can contain all the standard message properties such as the sender, the intended recipient, and when the message was sent.</span></span> <span data-ttu-id="f77c9-125">フォームには、フォームに固有の任意の数のカスタムプロパティを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-125">Forms can also contain any number of custom properties that are specific to the form.</span></span> <span data-ttu-id="f77c9-126">たとえば、"バグレポート" フォームには、バグの種類、バグの重大度、および製品バージョンのカスタムプロパティが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="f77c9-126">For example a "Bug Report" form might contain custom properties for Bug Type, Bug Severity, and Product Version.</span></span>
  
<span data-ttu-id="f77c9-127">フォームを作成するには、フォームサーバーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f77c9-127">To create a form you must implement a form server.</span></span> <span data-ttu-id="f77c9-128">フォームサーバーは、メッセージングクライアントがフォームサーバーでサポートされている種類のメッセージを表示する必要がある場合に読み込まれる実行可能ファイルです。</span><span class="sxs-lookup"><span data-stu-id="f77c9-128">The form server is the executable file that is loaded when a messaging client needs to display a message that is the type supported by the form server.</span></span> <span data-ttu-id="f77c9-129">その後、フォームサーバーは、必要に応じてフォームオブジェクトを作成し、特定のメッセージを表示して、それらのメッセージでのユーザー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-129">The form server in turn creates form objects as necessary to display specific messages and handle user interactions with those messages.</span></span>
  
<span data-ttu-id="f77c9-130">すべてのフォームサーバーには、構成ファイルが関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="f77c9-130">Every form server has a configuration file associated with it.</span></span> <span data-ttu-id="f77c9-131">このファイルには、フォームマネージャーの利点を得るためのフォームサーバーを説明する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f77c9-131">This file contains information that describes the form server for the benefit of the form manager.</span></span> <span data-ttu-id="f77c9-132">フォームマネージャーは、フォームサーバーをフォームライブラリにインストールするときにこの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-132">The form manager uses this information when installing the form server into a form library.</span></span>
  
<span data-ttu-id="f77c9-133">フォームのパーツを作成する方法の詳細については、「 [MAPI フォームサーバーの開発](developing-mapi-form-servers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f77c9-133">For details on creating the parts of a form, see [Developing MAPI Form Servers](developing-mapi-form-servers.md).</span></span>
  
<span data-ttu-id="f77c9-134">フォームサーバーは、コンポーネントオブジェクトモデル (COM) に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="f77c9-134">Form servers adhere to the Component Object Model (COM).</span></span> <span data-ttu-id="f77c9-135">フォームサーバーは、インプロセスサーバーとしてではなく、スタンドアロンの実行可能ファイルとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="f77c9-135">Form servers run as standalone executables, not as in-proc servers.</span></span> <span data-ttu-id="f77c9-136">詳細については、Windows SDK の「COM および ActiveX のオブジェクトサービス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f77c9-136">For more information, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
<span data-ttu-id="f77c9-137">一意のクラス識別子 (CLSID) は、各フォームサーバーを識別します。</span><span class="sxs-lookup"><span data-stu-id="f77c9-137">A unique class identifier (CLSID) identifies each form server.</span></span> <span data-ttu-id="f77c9-138">クラス識別子とそのメッセージクラスの間には、常に1対1のマッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="f77c9-138">There is always a one-to-one mapping between a class identifier and its message class.</span></span> <span data-ttu-id="f77c9-139">ただし、フォームサーバーは、1つのメッセージクラスのメッセージでしか動作できないことを意味するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="f77c9-139">This does not mean, however, that a form server can only work with messages of one message class.</span></span> <span data-ttu-id="f77c9-140">特定のクラスのメッセージを処理するためのフォームサーバーが利用できない場合、使用されているフォームマネージャーは、メッセージクラス階層内で上位にあるメッセージクラスのフォームサーバーの検索を試みる必要があります。Windows SDK で提供される既定のフォームマネージャーがこれを行います。</span><span class="sxs-lookup"><span data-stu-id="f77c9-140">If no form server is available to service a message of a particular class, the form manager being used should attempt to find a form server for a message class higher in the message class hierarchy; the default form manager supplied with the Windows SDK does this.</span></span> <span data-ttu-id="f77c9-141">このようなフォームサーバーは、おそらく、メッセージのプロパティ (スーパークラスでサポートされているもの) のサブセットのみを表示できるようになりますが、nothing よりも優れています。</span><span class="sxs-lookup"><span data-stu-id="f77c9-141">Such a form server will probably be able to render only a subset of the message's properties (the ones supported by the superclass), but it will be better than nothing.</span></span> <span data-ttu-id="f77c9-142">一致するフォームサーバーが見つからない場合は、使用されているフォームマネージャーに固有の実装の詳細が発生します。このイベントが発生した場合、既定のフォームマネージャーはメッセージを開きません。</span><span class="sxs-lookup"><span data-stu-id="f77c9-142">What happens when no matching form server is found at all is an implementation detail specific to the form manager being used; the default form manager does not open messages when this happens.</span></span>
  
<span data-ttu-id="f77c9-143">詳細については、「 [MAPI メッセージクラス](mapi-message-classes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f77c9-143">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f77c9-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="f77c9-144">See also</span></span>



[<span data-ttu-id="f77c9-145">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="f77c9-145">MAPI Forms</span></span>](mapi-forms.md)

