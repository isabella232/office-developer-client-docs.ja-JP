---
title: フォームの動詞
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424029"
---
# <a name="form-verbs"></a><span data-ttu-id="2762c-103">フォームの動詞</span><span class="sxs-lookup"><span data-stu-id="2762c-103">Form verbs</span></span>

<span data-ttu-id="2762c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2762c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2762c-105">フォームのユーザー インターフェイスには、通常、ユーザーがフォームに対して何らかのアクションを実行できるメニュー項目またはコントロールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="2762c-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="2762c-106">これらのユーザーアクションを処理するのがフォーム サーバーのジョブです。</span><span class="sxs-lookup"><span data-stu-id="2762c-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="2762c-107">このインターフェイスは、標準の Win32 API を使用して実装されます。1 つを記述する方法は、通常の Win32 プログラム用の他のインターフェイスを記述するのと同じ方法です。</span><span class="sxs-lookup"><span data-stu-id="2762c-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="2762c-108">多くの場合、ユーザーアクションは動詞に関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="2762c-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="2762c-109">動詞は、特定のメッセージ クラスに固有のアクションの名前です。</span><span class="sxs-lookup"><span data-stu-id="2762c-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="2762c-110">たとえば **、Reply** は多くのフォーム サーバーによって実装される動詞で、それぞれの動詞の解釈が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2762c-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="2762c-111">動詞はコマンドと呼ばれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2762c-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2762c-112">フォーム上のすべてのメニュー項目とコントロールが動詞に対応しているという場合があります。</span><span class="sxs-lookup"><span data-stu-id="2762c-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="2762c-113">たとえば、[キャンセル] **ボタン** はフォーム サーバー内の Cancel 動詞に対応しません。</span><span class="sxs-lookup"><span data-stu-id="2762c-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="2762c-114">通常、動詞は、特定のメッセージ クラスまたは一連のメッセージ クラスに固有のアクションに関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="2762c-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="2762c-115">異なるメッセージ クラスでさまざまな動詞セットをサポートすることもできますが、少なくとも Open 動詞はサポートされ、フォームのユーザー インターフェイスが表示され、メッセージのプロパティ値で読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="2762c-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="2762c-116">動詞はパラメーターを受け取らない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2762c-116">Verbs may take no parameters.</span></span> <span data-ttu-id="2762c-117">変数パラメーターを使用してコマンドをエクスポートするフォームでは、オートメーション メカニズムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2762c-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="2762c-118">クライアントは、MAPI フォーム マネージャーによって実装される [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) メソッドを使用して、特定のメッセージ クラスでサポートされる動詞を決定できます。</span><span class="sxs-lookup"><span data-stu-id="2762c-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="2762c-119">フォーム マネージャーは、フォームの構成ファイルからこの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="2762c-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="2762c-120">このメソッドによって返される動詞セットは、メッセージで実行できるコマンドをユーザーに表示するためにクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2762c-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="2762c-121">たとえば、クライアントを使用すると、ユーザーはメッセージの上でマウスの右ボタンをクリックして、そのメッセージに適用可能な動詞を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2762c-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2762c-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="2762c-122">See also</span></span>

- [<span data-ttu-id="2762c-123">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="2762c-123">MAPI Forms</span></span>](mapi-forms.md)

