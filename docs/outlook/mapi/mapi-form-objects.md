---
title: MAPI フォーム オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404786"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="69048-103">MAPI フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="69048-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="69048-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69048-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69048-105">フォーム オブジェクトは、特定のメッセージを表示し、ユーザーがそれらを操作するために、フォーム サーバーによって動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="69048-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="69048-106">したがって、フォーム オブジェクトは、フォーム サーバーによって実装される [IMAPIForm](imapiformiunknown.md) から派生したクラスのインスタンス化です。</span><span class="sxs-lookup"><span data-stu-id="69048-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="69048-107">クライアント アプリケーションがメッセージを開くと、そのメッセージ クラスのフォーム サーバーによって、メッセージを処理するフォーム オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="69048-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="69048-108">フォーム オブジェクトは、そのインターフェイスを作成し、その中にメッセージのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="69048-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="69048-109">フォーム オブジェクトとそのインターフェイスは、ユーザーが閉じるまで保持されます。</span><span class="sxs-lookup"><span data-stu-id="69048-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="69048-110">フォーム オブジェクトは、メッセージのプロパティの値に対する変更を処理します。</span><span class="sxs-lookup"><span data-stu-id="69048-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="69048-111">さらに、MAPI フォーム インターフェイスは、1 つのフォーム オブジェクトが一連のメッセージを読み込み、表示できるメカニズムを定義します。</span><span class="sxs-lookup"><span data-stu-id="69048-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="69048-112">これは、メッセージ オブジェクトとそのインターフェイスの不必要な破棄と作成を回避する効率メカニズムです。</span><span class="sxs-lookup"><span data-stu-id="69048-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="69048-113">メッセージング クライアントから別のメッセージの読み込みを要求された場合、フォーム オブジェクトは現在のメッセージのプロパティに対する変更を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69048-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="69048-114">クライアント アプリケーションのフォーム オブジェクトの観点については、「MAPI カスタム フォーム オブジェクト」 [を参照してください](mapi-custom-form-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="69048-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69048-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="69048-115">See also</span></span>



[<span data-ttu-id="69048-116">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="69048-116">MAPI Forms</span></span>](mapi-forms.md)

