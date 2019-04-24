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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327490"
---
# <a name="form-verbs"></a><span data-ttu-id="e1918-103">フォームの動詞</span><span class="sxs-lookup"><span data-stu-id="e1918-103">Form verbs</span></span>

<span data-ttu-id="e1918-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1918-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1918-105">通常、フォームのユーザーインターフェイスは、ユーザーがフォームに対して何らかのアクションを実行できるようにするメニュー項目またはコントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="e1918-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="e1918-106">これは、これらのユーザー操作を処理するフォームサーバーのジョブです。</span><span class="sxs-lookup"><span data-stu-id="e1918-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="e1918-107">このインターフェイスは、標準の Win32 api を使用して実装されています。1つの書き込みは、通常の Win32 プログラムの他のインターフェイスを記述するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="e1918-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="e1918-108">多くの場合、ユーザー操作は動詞に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="e1918-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="e1918-109">動詞は、特定のメッセージクラスに固有のアクションの名前です。</span><span class="sxs-lookup"><span data-stu-id="e1918-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="e1918-110">たとえば、 **Reply**は、多くのフォームサーバーによって実装されている動詞です。それぞれに、それぞれの動詞の解釈が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e1918-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="e1918-111">動詞は、コマンドと呼ばれることがあります。</span><span class="sxs-lookup"><span data-stu-id="e1918-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1918-112">フォーム上のすべてのメニュー項目とコントロールが動詞に対応するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="e1918-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="e1918-113">たとえば、 **[キャンセル**] ボタンは、フォームサーバー内の cancel 動詞には対応していません。</span><span class="sxs-lookup"><span data-stu-id="e1918-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="e1918-114">通常、動詞は特定のメッセージクラスまたは一連のメッセージクラスに固有のアクションに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="e1918-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="e1918-115">さまざまなメッセージクラスはさまざまな動詞のセットをサポートしていますが、すべては少なくとも、フォームのユーザーインターフェイスを表示し、メッセージのプロパティ値を使用して読み込む、Open 動詞をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e1918-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="e1918-116">動詞にはパラメーターを必要としない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e1918-116">Verbs may take no parameters.</span></span> <span data-ttu-id="e1918-117">変数パラメーターを使用してコマンドをエクスポートするフォームには、オートメーション機構を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1918-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="e1918-118">クライアントは、MAPI フォームマネージャーで実装されている[imapiforminfo:: CalcVerbSet](imapiforminfo-calcverbset.md)メソッドを使用して、特定のメッセージクラスでサポートされている動詞を特定できます。</span><span class="sxs-lookup"><span data-stu-id="e1918-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="e1918-119">フォームマネージャーは、この情報をフォームの構成ファイルから取得します。</span><span class="sxs-lookup"><span data-stu-id="e1918-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="e1918-120">このメソッドによって返される動詞セットは、メッセージに対して実行できるコマンドをユーザーに表示するためにクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="e1918-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="e1918-121">たとえば、クライアントでは、ユーザーがメッセージ上でマウスの右ボタンをクリックして、そのメッセージに適用される動詞を表示できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e1918-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1918-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1918-122">See also</span></span>

- [<span data-ttu-id="e1918-123">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="e1918-123">MAPI Forms</span></span>](mapi-forms.md)

