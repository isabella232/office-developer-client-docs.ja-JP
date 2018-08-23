---
title: フォームの動詞
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800100"
---
# <a name="form-verbs"></a><span data-ttu-id="8eb55-103">フォームの動詞</span><span class="sxs-lookup"><span data-stu-id="8eb55-103">Form verbs</span></span>

<span data-ttu-id="8eb55-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8eb55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8eb55-105">通常、フォームのユーザー インターフェイスは、メニュー項目、または何らかの形式でアクションを実行するユーザーを有効にするコントロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="8eb55-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="8eb55-106">これらのユーザー アクションを処理するためにフォームのサーバーの仕事です。</span><span class="sxs-lookup"><span data-stu-id="8eb55-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="8eb55-107">このインターフェイスは標準的な Win32 Api を使用します。標準の Win32 プログラムの他のインターフェイスの記述と同じようには 1 つを記述します。</span><span class="sxs-lookup"><span data-stu-id="8eb55-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="8eb55-108">多くの場合、ユーザーの操作では、動詞に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="8eb55-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="8eb55-109">動詞とは、特定のメッセージ クラスに固有であるアクションの名前です。</span><span class="sxs-lookup"><span data-stu-id="8eb55-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="8eb55-110">たとえば、**返信**は、その動詞のさまざまな解釈の可能性があります、多くのフォームのサーバーによって実装される動詞です。</span><span class="sxs-lookup"><span data-stu-id="8eb55-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="8eb55-111">動詞は、コマンドとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8eb55-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8eb55-112">すべてのメニュー項目や、フォーム上のコントロールは、動詞に対応しています。</span><span class="sxs-lookup"><span data-stu-id="8eb55-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="8eb55-113">たとえば、 **[キャンセル**] ボタンは、フォーム サーバー内での Cancel 動詞は対応していません。</span><span class="sxs-lookup"><span data-stu-id="8eb55-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="8eb55-114">通常、動詞は、特定のメッセージ クラスまたは一連のメッセージ クラスに固有のアクションに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="8eb55-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="8eb55-115">別のメッセージ クラスには、さまざまな動詞のセットをサポートできますが、すべてをサポートして、少なくとも、開いている動詞は、フォームのユーザー インターフェイスが表示され、読み込まれるときに、メッセージのプロパティの値を持つ。</span><span class="sxs-lookup"><span data-stu-id="8eb55-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="8eb55-116">動詞はパラメーターを受け取ることがない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8eb55-116">Verbs may take no parameters.</span></span> <span data-ttu-id="8eb55-117">フォーム変数のパラメーターを使用してコマンドをエクスポートするには、オートメーション メカニズムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8eb55-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="8eb55-118">クライアントでは、どの動詞が、MAPI フォーム マネージャーによって実装されている[IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドを特定のメッセージ クラスでサポートされているを確認できます。</span><span class="sxs-lookup"><span data-stu-id="8eb55-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="8eb55-119">フォーム マネージャーは、フォームの構成ファイルからこの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="8eb55-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="8eb55-120">このメソッドによって返される動詞のセットは、メッセージ上のコマンドを実行できるユーザーを表示するのには、クライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="8eb55-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="8eb55-121">たとえば、クライアントは、ユーザーがそのメッセージに適用可能な動詞を表示するメッセージをマウスの右ボタンをクリックするを有効にする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8eb55-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8eb55-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="8eb55-122">See also</span></span>

- [<span data-ttu-id="8eb55-123">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="8eb55-123">MAPI Forms</span></span>](mapi-forms.md)

