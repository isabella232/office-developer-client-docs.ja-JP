---
title: MAPI フォームのサーバー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: dad36bfc5fed296cff3baa4cc11bb1fdf359c45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801369"
---
# <a name="mapi-form-servers"></a><span data-ttu-id="df8b8-103">MAPI フォームのサーバー</span><span class="sxs-lookup"><span data-stu-id="df8b8-103">MAPI Form Servers</span></span>

  
  
<span data-ttu-id="df8b8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df8b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df8b8-105">ユーザーの観点からは、フォームと、メッセージ、または構造化された情報を入力するユーザーを有効にするデータ入力フォームのプロパティ シートでは通常。</span><span class="sxs-lookup"><span data-stu-id="df8b8-105">From the user's perspective, a form is usually a property sheet for a message or a data-entry form that enables users to enter structured information.</span></span> <span data-ttu-id="df8b8-106">ただし、メッセージ クラスに関連付けられているすべてのユーザー インターフェイスであることができます。</span><span class="sxs-lookup"><span data-stu-id="df8b8-106">However, it can be any user interface that is associated with a message class.</span></span> <span data-ttu-id="df8b8-107">プログラマの視点から、フォームで構成されます。</span><span class="sxs-lookup"><span data-stu-id="df8b8-107">From a programmer's point of view, a form consists of:</span></span>
  
- <span data-ttu-id="df8b8-108">独自のメッセージ クラスと OLE 識別子を持つ MAPI メッセージの種類。</span><span class="sxs-lookup"><span data-stu-id="df8b8-108">A type of MAPI message with its own message class and OLE identifier.</span></span>
    
- <span data-ttu-id="df8b8-109">フォーム サーバーを実装する実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="df8b8-109">The executable file that implements the form server.</span></span>
    
- <span data-ttu-id="df8b8-110">MAPI プロパティのコレクション: カスタムまたはそれ以外の場合、フォームのサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-110">A collection of MAPI properties — custom or otherwise — that the form server uses.</span></span> <span data-ttu-id="df8b8-111">これらの一部またはすべてを使用するメッセージング クライアントが利用できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="df8b8-111">Some or all of these may be available to messaging clients for use.</span></span>
    
- <span data-ttu-id="df8b8-112">フォームを説明し、フォーム マネージャーを使用する構成ファイルです。</span><span class="sxs-lookup"><span data-stu-id="df8b8-112">The configuration file that describes the form and is used by the form manager.</span></span>
    
<span data-ttu-id="df8b8-113">フォームは[IMessage](imessageimapiprop.md)オブジェクトであるため、プロパティおよび MAPI メッセージ オブジェクトに一貫性のある動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-113">Because forms are [IMessage](imessageimapiprop.md) objects, they exhibit properties and behavior that is consistent with MAPI message objects.</span></span> <span data-ttu-id="df8b8-114">ただし、フォームには、カスタム プロパティ、コントロール、およびアプリケーションに固有であるディスプレイの表示を持つことができます、ため使用を形成する MAPI インターフェイスは汎用性が必要なインターフェイスの任意の種類を許可します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-114">However, because forms can have custom properties, controls, and a display rendering that is application-specific, the MAPI interfaces that forms use are generic enough to permit any sort of interface that is needed.</span></span> <span data-ttu-id="df8b8-115">フォームの実際の定義は、このセクションで後述する、フォーム ライブラリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="df8b8-115">The actual definition of a form is stored in a form library, which is discussed later in this section.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="df8b8-116">正確に、すべてのメッセージは、MAPI フォームのインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="df8b8-116">More accurately, all messages are instances of MAPI forms.</span></span> <span data-ttu-id="df8b8-117">ただし、通常と考えるユーザー設定フォームのメッセージの特殊なケースを作成するためのフォームから簡単に、一般的な電子メール メッセージの読み取りは、最もよく使用される形式です。</span><span class="sxs-lookup"><span data-stu-id="df8b8-117">However, it is usually easier to think of custom forms as special cases of messages, since forms for composing and reading typical email messages are the most commonly used forms.</span></span> <span data-ttu-id="df8b8-118">すべてのメッセージには、カスタムのフォームは実際にはということは、MAPI システムで、他のメッセージと同様にステータスを形成します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-118">The fact that all messages are really just forms gives custom forms the same status as any other message in the MAPI system.</span></span> 
  
<span data-ttu-id="df8b8-119">すべてのフォームには、いくつかは、フォームのユーザー インターフェイスに表示されているプロパティのセットがあります。</span><span class="sxs-lookup"><span data-stu-id="df8b8-119">Every form has a set of properties, some of which are visible in the form's user interface.</span></span> <span data-ttu-id="df8b8-120">通常、プロパティは、フォームのユーザー インターフェイス内のフィールドに一致します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-120">Usually, properties are matched to fields in the form's user interface.</span></span> <span data-ttu-id="df8b8-121">たとえば、発注書フォームでは、アイテム、説明、価格、税、および集計フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="df8b8-121">For example, a purchase order form might have the fields Item, Description, Price, Tax, and Subtotal.</span></span> <span data-ttu-id="df8b8-122">これらのフィールドは、同じ名前のフォームのプロパティを視覚的にレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="df8b8-122">These fields are simply visual renderings of form properties of the same names.</span></span> <span data-ttu-id="df8b8-123">クライアントは、どのプロパティが MAPI フォーム マネージャーによって実装されている[IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)メソッドは、特定のメッセージ クラスでサポートされているを確認します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-123">Clients ascertain which properties are supported by a particular message class through the [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) method, which is implemented by the MAPI form manager.</span></span> 
  
<span data-ttu-id="df8b8-124">基本的なメッセージは、のような MAPI フォームが目的の受信者、送信者などのすべての標準的なメッセージ プロパティを含めることができ、メッセージが送信されました。</span><span class="sxs-lookup"><span data-stu-id="df8b8-124">Like basic messages, MAPI forms can contain all the standard message properties such as the sender, the intended recipient, and when the message was sent.</span></span> <span data-ttu-id="df8b8-125">フォームは、フォームに固有のカスタム プロパティの任意の数を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="df8b8-125">Forms can also contain any number of custom properties that are specific to the form.</span></span> <span data-ttu-id="df8b8-126">たとえば「バグの報告書」フォームでは、バグ、バグの重要度、および製品のバージョンのカスタム プロパティを含めることが。</span><span class="sxs-lookup"><span data-stu-id="df8b8-126">For example a "Bug Report" form might contain custom properties for Bug Type, Bug Severity, and Product Version.</span></span>
  
<span data-ttu-id="df8b8-127">フォームを作成するには、フォーム サーバーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8b8-127">To create a form you must implement a form server.</span></span> <span data-ttu-id="df8b8-128">フォーム サーバーは、メッセージング クライアントは、フォームのサーバーでサポートされている型であるメッセージを表示する必要がある場合に読み込まれる実行可能ファイルです。</span><span class="sxs-lookup"><span data-stu-id="df8b8-128">The form server is the executable file that is loaded when a messaging client needs to display a message that is the type supported by the form server.</span></span> <span data-ttu-id="df8b8-129">フォーム サーバーに特定のメッセージを表示し、それらのメッセージを持つユーザーとのやり取りを処理する必要に応じて、フォーム オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-129">The form server in turn creates form objects as necessary to display specific messages and handle user interactions with those messages.</span></span>
  
<span data-ttu-id="df8b8-130">フォームのすべてのサーバーでは、それに関連する構成ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="df8b8-130">Every form server has a configuration file associated with it.</span></span> <span data-ttu-id="df8b8-131">このファイルには、フォームのマネージャーのためのフォームのサーバーを記述する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df8b8-131">This file contains information that describes the form server for the benefit of the form manager.</span></span> <span data-ttu-id="df8b8-132">フォーム マネージャーは、フォーム ライブラリにフォームのサーバーをインストールするときにこの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-132">The form manager uses this information when installing the form server into a form library.</span></span>
  
<span data-ttu-id="df8b8-133">フォームの一部を作成する方法の詳細については、 [MAPI フォームのサーバーの開発](developing-mapi-form-servers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df8b8-133">For details on creating the parts of a form, see [Developing MAPI Form Servers](developing-mapi-form-servers.md).</span></span>
  
<span data-ttu-id="df8b8-134">フォームのサーバーは、コンポーネント オブジェクト モデル (COM) に準拠します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-134">Form servers adhere to the Component Object Model (COM).</span></span> <span data-ttu-id="df8b8-135">フォームのサーバーをインプロセス サーバーとしてではなく、スタンドアロンの実行ファイルとして実行します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-135">Form servers run as standalone executables, not as in-proc servers.</span></span> <span data-ttu-id="df8b8-136">詳細については、Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="df8b8-136">For more information, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
<span data-ttu-id="df8b8-137">一意のクラス識別子 (CLSID) では、各フォームのサーバーを識別します。</span><span class="sxs-lookup"><span data-stu-id="df8b8-137">A unique class identifier (CLSID) identifies each form server.</span></span> <span data-ttu-id="df8b8-138">クラス id と、メッセージ クラスとの間の 1 対 1 マッピングでは常にします。</span><span class="sxs-lookup"><span data-stu-id="df8b8-138">There is always a one-to-one mapping between a class identifier and its message class.</span></span> <span data-ttu-id="df8b8-139">ありません、ただし、フォーム サーバーが 1 つのメッセージ クラスのメッセージを操作できますのみです。</span><span class="sxs-lookup"><span data-stu-id="df8b8-139">This does not mean, however, that a form server can only work with messages of one message class.</span></span> <span data-ttu-id="df8b8-140">フォーム マネージャーを使用している必要があるメッセージ クラスの階層構造内の上位のメッセージ クラスのフォームのサーバーを検索しようとして特定のクラスのメッセージを処理するために利用可能なフォームのサーバーがない場合は、Windows SDK に付属している既定のフォーム マネージャーは実行されます。</span><span class="sxs-lookup"><span data-stu-id="df8b8-140">If no form server is available to service a message of a particular class, the form manager being used should attempt to find a form server for a message class higher in the message class hierarchy; the default form manager supplied with the Windows SDK does this.</span></span> <span data-ttu-id="df8b8-141">フォームのサーバーはメッセージのプロパティ (スーパークラスでサポートされているもの) のサブセットのみを表示することが、何もないよりは良いことが。</span><span class="sxs-lookup"><span data-stu-id="df8b8-141">Such a form server will probably be able to render only a subset of the message's properties (the ones supported by the superclass), but it will be better than nothing.</span></span> <span data-ttu-id="df8b8-142">一致するフォームのサーバーが見つからなかった場合は、使用されるフォーム マネージャーに固有の実装の詳細このような場合、既定のフォーム マネージャーはメッセージを開きません。</span><span class="sxs-lookup"><span data-stu-id="df8b8-142">What happens when no matching form server is found at all is an implementation detail specific to the form manager being used; the default form manager does not open messages when this happens.</span></span>
  
<span data-ttu-id="df8b8-143">詳細については、 [MAPI メッセージ クラス](mapi-message-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df8b8-143">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df8b8-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="df8b8-144">See also</span></span>



[<span data-ttu-id="df8b8-145">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="df8b8-145">MAPI Forms</span></span>](mapi-forms.md)

