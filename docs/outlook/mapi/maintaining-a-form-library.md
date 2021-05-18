---
title: フォーム ライブラリの保守
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408804"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="ff85e-103">フォーム ライブラリの保守</span><span class="sxs-lookup"><span data-stu-id="ff85e-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="ff85e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff85e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff85e-105">フォーム ライブラリには、フォームのプロパティ、動詞、サーバーの実行可能ファイルなど、フォームに関する重要な情報すべてが保持されます。</span><span class="sxs-lookup"><span data-stu-id="ff85e-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="ff85e-106">一部のクライアントでは、ユーザーがフォーム サーバーを保守、インストール、または削除できます。</span><span class="sxs-lookup"><span data-stu-id="ff85e-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="ff85e-107">この機能をユーザーに提供する場合は、次の機能にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff85e-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="ff85e-108">フォーム サーバーの構成ファイル、.CFG 拡張機能。</span><span class="sxs-lookup"><span data-stu-id="ff85e-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="ff85e-109">フォーム ライブラリのコンテナー オブジェクト [、IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) インターフェイスを実装するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ff85e-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="ff85e-110">構成ファイルまたはパス名にアクセスするには、便利な手段を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="ff85e-111">通常、クライアントは、構成ファイルの場所をユーザーに確認するフォーム サーバーをインストールおよび削除するためのダイアログ ボックスをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="ff85e-112">フォーム ライブラリのコンテナーにアクセスするには、フォーム マネージャーの [IMAPIFormMgr::OpenFormContainer メソッドを呼び出](imapiformmgr-openformcontainer.md) します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="ff85e-113">列挙値を渡して、開くフォーム ライブラリを指定し、必要に応じてフォーム マネージャーがフォーム ライブラリを開くのに使用するオブジェクトへのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="ff85e-114">たとえば、フォルダー フォーム ライブラリを[](folder-form-libraries.md)開く場合は[、IMAPIFolder : IMAPIContainer ポインターを渡](imapifolderimapicontainer.md)します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="ff85e-115">**OpenFormContainer** が **IMAPIFormContainer** ポインターを返した後、実行するメンテナンスに応じて [、IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)または [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="ff85e-116">**InstallForm** は、フォーム サーバーをライブラリに追加します。 **RemoveForm** は、フォーム サーバーをライブラリから削除します。</span><span class="sxs-lookup"><span data-stu-id="ff85e-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

