---
title: ライブラリへのフォームのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433144"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="e60ea-103">ライブラリへのフォームのインストール</span><span class="sxs-lookup"><span data-stu-id="e60ea-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="e60ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e60ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e60ea-105">Windows SDK で提供される既定の MAPI フォームマネージャーは、さまざまなフォームライブラリにフォームをインストールするためのユーザーインターフェイスを提供しません。</span><span class="sxs-lookup"><span data-stu-id="e60ea-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="e60ea-106">このため、ユーザーがフォームのインストールに使用できる小さなアプリケーションまたは詳細な手順のセットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e60ea-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="e60ea-107">インストールアプリケーションを実装する場合、フォームをフォルダーに関連付けられたコンテンツテーブルにインストールするために実行する必要がある一連のアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e60ea-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="e60ea-108">[MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出して、フォームマネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e60ea-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="e60ea-109">[imapiformmgr:: openformcontainer](imapiformmgr-openformcontainer.md)または[imapiformmgr:: selectformcontainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、フォームのターゲットコンテナーを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="e60ea-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="e60ea-110">[imapiformcontainer:: installform](imapiformcontainer-installform.md)関数を使用して、フォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e60ea-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="e60ea-111">手順 4 ~ 6 は、ローカルフォームライブラリへのインストールに使用できます。</span><span class="sxs-lookup"><span data-stu-id="e60ea-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="e60ea-112">インストールがユーザーのワークステーション上のローカルフォームライブラリにインストールされている場合は、すべてのファイルをローカルディスク上の適切な場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="e60ea-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="e60ea-113">必要に応じて、コンポーネントの現在のパスを反映するようにフォーム構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="e60ea-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="e60ea-114">フォーム構成ファイルには相対パスを含めることができます。この場合、この手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e60ea-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="e60ea-115">適切な OLE 登録手順を実行して、メッセージの種類とインストールされているフォームサーバーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="e60ea-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="e60ea-116">フォームがローカルフォームライブラリにインストールされている場合は、フォームのアイコン (.ico) ファイルと構成ファイル (cfg) を%WINDOWS%\FORMS\CONFIGS ディレクトリにコピーして、フォームライブラリが破損または削除された場合に、フォームを自動的に復元できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e60ea-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="e60ea-117">この手順は推奨されていますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e60ea-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e60ea-118">手順1と2を[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数の呼び出しで置き換えることにより、ローカルフォームライブラリへのインストールを簡素化できます。</span><span class="sxs-lookup"><span data-stu-id="e60ea-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e60ea-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="e60ea-119">See also</span></span>



[<span data-ttu-id="e60ea-120">MAPI フォームサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="e60ea-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

