---
title: MAPI フォームサーバーコードと Windows コードの統合
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332180"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="7fcd1-103">MAPI フォームサーバーコードと Windows コードの統合</span><span class="sxs-lookup"><span data-stu-id="7fcd1-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="7fcd1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fcd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fcd1-105">フォームサーバーが Win32 アプリケーションであることを思い出してください。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="7fcd1-106">そのため、フォームサーバーをメモリに読み込み、クリーンに終了することに関連するタスクがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="7fcd1-107">すべての Windows アプリケーションと同様に、フォームサーバーのエントリポイントは**WinMain**関数です。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="7fcd1-108">この関数は、次のタスクを実行するための適切な場所です。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="7fcd1-109">フォームサーバーが他の OLE コンポーネントと対話できるように、ウィンドウクラスを作成して登録します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="7fcd1-110">form オブジェクトのユーザーインターフェイス用のウィンドウクラスまたはクラスを作成して登録します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="7fcd1-111">[MAPIInitialize](mapiinitialize.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="7fcd1-112">**MAPIInitialize**では、必要な OLE 初期化も同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="7fcd1-113">これは、フォームサーバーのインスタンスごとに1回実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="7fcd1-114">フォームサーバーのクラス識別子 (CLSID) の文字列表記を使用して、グローバルアトムを登録します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="7fcd1-115">この atom は、フォームサーバーの有効期間中は存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="7fcd1-116">ole 関数[CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx)を呼び出して、ole を使用してフォームサーバーのクラスファクトリを登録します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="7fcd1-117">メッセージを受信するためのメインウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="7fcd1-118">このウィンドウは、ユーザーが個々の form オブジェクトに関連付けられている特定のウィンドウと対話するため、表示されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="7fcd1-119">ただし、開発時に、メインウィンドウは、フォームサーバーの出力やコントロールをデバッグするための便利な場所になることがあります。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="7fcd1-120">フォームサーバーの有効期間中に実行されるメッセージループを作成し、windows メッセージをアクティブな form オブジェクトに変換してディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="7fcd1-121">フォームサーバーが終了すると、次のタスクが実行されます。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="7fcd1-122">ole 関数[CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx)を呼び出して、メッセージクラスの ole 登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="7fcd1-123">**MAPIUninitialize**を呼び出して、フォームサーバーの MAPI への接続を適切に閉じます。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="7fcd1-124">クラス識別子の文字列表現を含むグローバルアトムを削除します。</span><span class="sxs-lookup"><span data-stu-id="7fcd1-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fcd1-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fcd1-125">See also</span></span>



[<span data-ttu-id="7fcd1-126">フォームサーバーコードの記述</span><span class="sxs-lookup"><span data-stu-id="7fcd1-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

