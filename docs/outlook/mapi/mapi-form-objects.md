---
title: MAPI フォーム オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0cece598d4ad337e29edb3bb98b302de900e056d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593467"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="50032-103">MAPI フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="50032-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="50032-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50032-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50032-105">フォーム オブジェクトは、特定のメッセージを表示し、それらと対話できるようにするためにフォームのサーバーによって動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="50032-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="50032-106">フォーム オブジェクトは、フォーム サーバーが実装されている[IMAPIForm](imapiformiunknown.md)から派生したクラスのインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="50032-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="50032-107">クライアント アプリケーションは、メッセージを開き、そのメッセージ クラスのフォームのサーバーは、メッセージを処理するフォーム オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="50032-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="50032-108">フォーム オブジェクトは、そのインタ フェースを作成し、メッセージのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="50032-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="50032-109">フォーム オブジェクトとそのインタ フェースは、ユーザーが閉じるまでに永続化されます。</span><span class="sxs-lookup"><span data-stu-id="50032-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="50032-110">フォーム オブジェクトは、メッセージのプロパティの値への変更を処理します。</span><span class="sxs-lookup"><span data-stu-id="50032-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="50032-111">さらに、MAPI フォームのインタ フェースは、1 つのフォーム オブジェクトを読み込むし、一連のメッセージを表示する機構を定義します。</span><span class="sxs-lookup"><span data-stu-id="50032-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="50032-112">これは、言うまでもなく破壊し、メッセージのオブジェクトとそのインターフェイスの作成を回避できるので、効率性のメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="50032-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="50032-113">メッセージング クライアントによって要求されると別のメッセージをロードするのには、form オブジェクトは現在のメッセージのプロパティに変更を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50032-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="50032-114">フォーム オブジェクトのクライアント アプリケーションの観点については、 [MAPI ユーザー設定のフォーム オブジェクト](mapi-custom-form-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50032-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50032-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="50032-115">See also</span></span>



[<span data-ttu-id="50032-116">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="50032-116">MAPI Forms</span></span>](mapi-forms.md)

