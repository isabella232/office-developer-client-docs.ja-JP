---
title: MAPI フォームオブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351465"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="e6d62-103">MAPI フォームオブジェクト</span><span class="sxs-lookup"><span data-stu-id="e6d62-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="e6d62-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6d62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6d62-105">フォームオブジェクトは、フォームサーバーによって動的に作成され、特定のメッセージを表示したり、ユーザーがそれらを操作したりできるようになります。</span><span class="sxs-lookup"><span data-stu-id="e6d62-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="e6d62-106">そのため、form オブジェクトは、フォームサーバーによって実装されている[imapiform](imapiformiunknown.md)から派生したクラスのインスタンス化を行います。</span><span class="sxs-lookup"><span data-stu-id="e6d62-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="e6d62-107">クライアントアプリケーションがメッセージを開くと、そのメッセージクラスのフォームサーバーがメッセージを処理するためのフォームオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e6d62-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="e6d62-108">その後、form オブジェクトはそのインターフェイスを作成し、メッセージのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="e6d62-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="e6d62-109">form オブジェクトとそのインターフェイスは、ユーザーがそれを閉じるまで保持されます。</span><span class="sxs-lookup"><span data-stu-id="e6d62-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="e6d62-110">form オブジェクトは、メッセージのプロパティの値に対するすべての変更を処理します。</span><span class="sxs-lookup"><span data-stu-id="e6d62-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="e6d62-111">さらに、MAPI フォームインターフェイスは、1つの form オブジェクトが一連のメッセージを読み込んで表示できるメカニズムを定義します。</span><span class="sxs-lookup"><span data-stu-id="e6d62-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="e6d62-112">これは、不必要な消滅や、メッセージオブジェクトとそのインターフェイスの作成を回避することで、効率のメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="e6d62-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="e6d62-113">別のメッセージを読み込むために、メッセージングクライアントによって要求された場合、form オブジェクトは現在のメッセージのプロパティに対する変更を保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6d62-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="e6d62-114">クライアントアプリケーションによるフォームオブジェクトの視点については、「 [MAPI カスタムフォームオブジェクト](mapi-custom-form-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6d62-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6d62-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e6d62-115">See also</span></span>



[<span data-ttu-id="e6d62-116">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="e6d62-116">MAPI Forms</span></span>](mapi-forms.md)

