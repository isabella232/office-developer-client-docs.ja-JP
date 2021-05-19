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
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="871e9-103">ライブラリへのフォームのインストール</span><span class="sxs-lookup"><span data-stu-id="871e9-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="871e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="871e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="871e9-105">WINDOWS SDK に付属する既定の MAPI フォーム マネージャーは、さまざまなフォーム ライブラリにフォームをインストールするユーザー インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="871e9-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="871e9-106">この理由から、ユーザーがフォームのインストールに使用できる小さなアプリケーション (または手順の詳細なセット) を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="871e9-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="871e9-107">インストール アプリケーションを実装する場合、フォルダーに関連付けられたコンテンツ テーブルにフォームをインストールするために実行する必要がある一連のアクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="871e9-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="871e9-108">[MAPIOpenFormMgr 関数を呼び](mapiopenformmgr.md)出して、フォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="871e9-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="871e9-109">[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)または[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、フォームのターゲット コンテナーを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="871e9-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="871e9-110">[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)関数を使用してフォームをインストールします。</span><span class="sxs-lookup"><span data-stu-id="871e9-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="871e9-111">手順 4 ~ 6 は、ローカル フォーム ライブラリにインストールするための手順です。</span><span class="sxs-lookup"><span data-stu-id="871e9-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="871e9-112">インストールがユーザーのワークステーションのローカル フォーム ライブラリにインストールされている場合は、すべてのファイルをローカル ディスク上の適切な場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="871e9-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="871e9-113">必要に応じて、フォーム構成ファイルを変更して、コンポーネントの現在のパスを反映します。</span><span class="sxs-lookup"><span data-stu-id="871e9-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="871e9-114">フォーム構成ファイルには相対パスを含め、その場合、この手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="871e9-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="871e9-115">適切な OLE 登録手順を実行して、メッセージの種類をインストール中のフォーム サーバーに関連付ける。</span><span class="sxs-lookup"><span data-stu-id="871e9-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="871e9-116">フォームがローカル フォーム ライブラリにインストールされている場合は、フォーム ライブラリが破損または削除された場合にフォームを自動的に復元できるよう、フォームのアイコン (.ico) および構成 (.cfg) ファイルを %WINDOWS%\FORMS\CONFIGS ディレクトリにコピーします。</span><span class="sxs-lookup"><span data-stu-id="871e9-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="871e9-117">この手順は推奨されますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="871e9-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="871e9-118">手順 1 と 2 を [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) 関数の呼び出しに置き換え、ローカル フォーム ライブラリへのインストールを簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="871e9-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="871e9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="871e9-119">See also</span></span>



[<span data-ttu-id="871e9-120">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="871e9-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

