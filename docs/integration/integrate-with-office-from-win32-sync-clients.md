---
title: Win32 同期クライアントからの Office との統合
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: サード パーティ製 Win32 同期クライアントを Excel Mobile、 PowerPoint Mobile、および Word MobileOffice アプリケーションと統合します。
ms.openlocfilehash: 83bc6e4cddc17e539b371999fff620c72c595534
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303137"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a><span data-ttu-id="370e6-103">Win32 同期クライアントからの Office との統合</span><span class="sxs-lookup"><span data-stu-id="370e6-103">Integrate with Office from Win32 sync clients</span></span>

<span data-ttu-id="370e6-104">サード パーティ製 Win32 同期クライアントを Excel Mobile、 PowerPoint Mobile、および Word MobileOffice アプリケーションと統合します。</span><span class="sxs-lookup"><span data-stu-id="370e6-104">Integrate your third-party Win32 sync clients with Excel Mobile, PowerPoint Mobile, and Word Mobile Office applications.</span></span> 
  
<span data-ttu-id="370e6-p101">同期ルート プロバイダーとして登録することにより、Windows ユニバーサル アプリを Excel Mobile、PowerPoint Mobile、および Word Mobile クライアントと統合できます。 この記事では、Win32 同期クライアントが Office アプリケーションと共に適切に動作するようにするため、適用できるベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="370e6-p101">You can integrate your Windows universal app with Excel Mobile, PowerPoint Mobile, and Word Mobile clients by registering as a sync root provider. This article describes the best practices to apply to ensure that your Win32 sync clients work well with Office applications.</span></span>
  
<span data-ttu-id="370e6-107">この統合では、Win32 同期クライアントに同期エンジンがあることが必要です。</span><span class="sxs-lookup"><span data-stu-id="370e6-107">This integration requires that your Win32 sync client has a sync engine.</span></span>
  
## <a name="register-as-a-sync-root-provider"></a><span data-ttu-id="370e6-108">同期ルート プロバイダーとして登録する</span><span class="sxs-lookup"><span data-stu-id="370e6-108">Register as a sync root provider</span></span>

<span data-ttu-id="370e6-p102">同期クライアントが同期ルート プロバイダーとして登録されていない限り、Office は同期フォルダー内のファイルを通常のローカル ファイルと同様の方法で扱います。つまり、ユーザーがドキュメントを共有しようとすると、Office は「OneDrive に移動する」オプションを示します。同期するファイルでこれを回避するには、同期ルート プロバイダーとして登録する必要があります。登録する方法について詳しくは、「[クラウド ストレージ プロバイダーの統合](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="370e6-p102">Unless your sync client is registered as a sync root provider, Office will treat files in your sync folder the way that it treats regular local files. This means that Office will provide "move to OneDrive" options for users when they attempt to share the document. To avoid this for files you sync, you must register as a sync root provider. For information about how to register, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span>
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a><span data-ttu-id="370e6-113">アプリをナビゲーション ウィンドウのルート ノードに統合する</span><span class="sxs-lookup"><span data-stu-id="370e6-113">Integrate your app into the root node of the navigation pane</span></span>

<span data-ttu-id="370e6-p103">Win32 同期クライアントがファイル エクスプ ローラーと Windows ファイル ピッカーでルート ノードとして表示されるようにするには、アプリをルート レベルに統合する必要があります。これを行う方法については、「[クラウド ストレージ プロバイダーの統合](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="370e6-p103">In order for your Win32 sync client to show up as a root node in the navigation pane in the File Explorer and Windows file picker, you need to integrate your app into the root level. For information about how to do this, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span> 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a><span data-ttu-id="370e6-116">同期フォルダーをドキュメント ライブラリとして追加する (省略可能)</span><span class="sxs-lookup"><span data-stu-id="370e6-116">Add your sync folder as a document library (optional)</span></span>

<span data-ttu-id="370e6-p104">Office で、ユーザーは単一の操作でドキュメント ライブラリにドキュメントを作成できます。ドキュメント ライブラリに同期場所に追加するには、[SHAddFolderPathToLibrary 関数](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx)を使用します。</span><span class="sxs-lookup"><span data-stu-id="370e6-p104">In Office, users can create documents in their document libraries with a single action. To add your sync location to the document library, use the [SHAddFolderPathToLibrary function](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="370e6-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="370e6-119">See also</span></span>
<span data-ttu-id="370e6-120"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="370e6-120"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="370e6-121">Office との統合</span><span class="sxs-lookup"><span data-stu-id="370e6-121">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="370e6-122">Windows ユニバーサル アプリからの Office との統合</span><span class="sxs-lookup"><span data-stu-id="370e6-122">Integrate with Office from Windows universal apps</span></span>](integrate-with-office-from-windows-universal-apps.md)
    

