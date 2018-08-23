---
title: ライブラリへのフォームのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d3b20c9fb4b4f1a26eb4ed1a9a498bd56a915a70
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579782"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="031c3-103">ライブラリへのフォームのインストール</span><span class="sxs-lookup"><span data-stu-id="031c3-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="031c3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="031c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="031c3-105">Windows SDK に付属している既定の MAPI フォーム マネージャーでは、各種のフォーム ライブラリにフォームをインストールするためのユーザー インターフェイスを行いません。</span><span class="sxs-lookup"><span data-stu-id="031c3-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="031c3-106">このため、小規模なアプリケーションを作成する必要がある、または一連の命令の詳細: ユーザーがフォームをインストールするのには使用できます。</span><span class="sxs-lookup"><span data-stu-id="031c3-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="031c3-107">インストール アプリケーションを実装する場合、一連のアクションを実行する必要の表は、次のとおりのフォルダーの関連する内容にフォームをインストールするのには。</span><span class="sxs-lookup"><span data-stu-id="031c3-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="031c3-108">マネージャーを開くには、フォームの[MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="031c3-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="031c3-109">[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)または[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、選択し、フォームの移動先のコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="031c3-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="031c3-110">フォームをインストールするのにには、 [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="031c3-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="031c3-111">4 ~ 6 の手順は、ローカルのフォーム ライブラリにインストールのことです。</span><span class="sxs-lookup"><span data-stu-id="031c3-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="031c3-112">インストールがユーザーのワークステーション上のローカル フォーム ライブラリにある場合は、ローカル ディスク上の適切な場所にすべてのファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="031c3-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="031c3-113">必要に応じて、コンポーネントの現在のパスを反映するようにフォーム構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="031c3-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="031c3-114">フォーム構成ファイルは、場合にこの手順は必要ありません、相対パスを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="031c3-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="031c3-115">インストールされているフォームのサーバーにメッセージの種類を関連付けるには、適切な OLE 登録手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="031c3-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="031c3-116">ローカル フォーム ライブラリにフォームがインストールされた場合、フォームのアイコン (.ico) と構成 (.cfg) ファイル ディレクトリにコピー、%WINDOWS%\FORMS\CONFIGS フォーム復元できるように自動的にフォーム ライブラリが破損または削除された場合にします。</span><span class="sxs-lookup"><span data-stu-id="031c3-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="031c3-117">この手順は、推奨されるが、必須ではないです。</span><span class="sxs-lookup"><span data-stu-id="031c3-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="031c3-118">手順 1 と 2 を[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数の呼び出しに置き換えることによって、ローカルのフォーム ライブラリにインストールを簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="031c3-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="031c3-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="031c3-119">See also</span></span>



[<span data-ttu-id="031c3-120">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="031c3-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

