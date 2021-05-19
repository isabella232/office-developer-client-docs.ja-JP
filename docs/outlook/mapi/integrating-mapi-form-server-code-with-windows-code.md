---
title: MAPI フォーム サーバー コードとサーバー コードWindowsする
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
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="46d44-103">MAPI フォーム サーバー コードとサーバー コードWindowsする</span><span class="sxs-lookup"><span data-stu-id="46d44-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="46d44-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46d44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46d44-105">フォーム サーバーが Win32 アプリケーションである点を思い出してください。</span><span class="sxs-lookup"><span data-stu-id="46d44-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="46d44-106">そのため、フォーム サーバーのメモリへの読み込みとクリーンな終了に関連するタスクがあります。</span><span class="sxs-lookup"><span data-stu-id="46d44-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="46d44-107">すべてのアプリケーションWindows同様に、フォーム サーバーのエントリ ポイントは **WinMain 関数** です。</span><span class="sxs-lookup"><span data-stu-id="46d44-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="46d44-108">この関数は、次のタスクを実行するための適切な場所です。</span><span class="sxs-lookup"><span data-stu-id="46d44-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="46d44-109">フォーム サーバーが他の OLE コンポーネントと対話できるよう、ウィンドウ クラスを作成および登録します。</span><span class="sxs-lookup"><span data-stu-id="46d44-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="46d44-110">フォーム オブジェクトのユーザー インターフェイス用のウィンドウ クラスまたはクラスの作成と登録。</span><span class="sxs-lookup"><span data-stu-id="46d44-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="46d44-111">[MAPIInitialize 関数を呼び出](mapiinitialize.md)します。</span><span class="sxs-lookup"><span data-stu-id="46d44-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="46d44-112">**MAPIInitialize は** 、必要な OLE 初期化も処理します。</span><span class="sxs-lookup"><span data-stu-id="46d44-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="46d44-113">これは、フォーム サーバーのインスタンスごとに 1 回実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46d44-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="46d44-114">フォーム サーバーのクラス識別子 (CLSID) の文字列表現を使用してグローバルアトムを登録する。</span><span class="sxs-lookup"><span data-stu-id="46d44-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="46d44-115">この atom は、フォーム サーバーの有効期間内に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46d44-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="46d44-116">OLE 関数 [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) を呼び出して、フォーム サーバーのクラス ファクトリを OLE に登録します。</span><span class="sxs-lookup"><span data-stu-id="46d44-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="46d44-117">メッセージを受信するためのメイン ウィンドウの作成。</span><span class="sxs-lookup"><span data-stu-id="46d44-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="46d44-118">このウィンドウは、ユーザーが個々のフォーム オブジェクトに関連付けられている特定のウィンドウを操作する場合なので、表示する必要はない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="46d44-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="46d44-119">ただし、開発中にメイン ウィンドウは、フォーム サーバーの出力または制御をデバッグする際に便利な場所になります。</span><span class="sxs-lookup"><span data-stu-id="46d44-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="46d44-120">フォーム サーバーの有効期間中に実行されるメッセージ ループを作成し、Windows メッセージをアクティブなフォーム オブジェクトに変換してディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="46d44-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="46d44-121">フォーム サーバーが終了すると、次のタスクが実行されます。</span><span class="sxs-lookup"><span data-stu-id="46d44-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="46d44-122">OLE 関数 [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) を呼び出して、メッセージ クラスの OLE 登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="46d44-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="46d44-123">**MAPIUninitialize を呼び** 出して、MAPI へのフォーム サーバーの接続を適切に閉じます。</span><span class="sxs-lookup"><span data-stu-id="46d44-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="46d44-124">クラス識別子の文字列表現を含むグローバルアトムを削除します。</span><span class="sxs-lookup"><span data-stu-id="46d44-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46d44-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="46d44-125">See also</span></span>



[<span data-ttu-id="46d44-126">フォーム サーバー コードの作成</span><span class="sxs-lookup"><span data-stu-id="46d44-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

