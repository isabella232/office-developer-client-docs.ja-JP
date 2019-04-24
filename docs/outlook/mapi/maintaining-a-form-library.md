---
title: フォームライブラリの管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298461"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="79653-103">フォームライブラリの管理</span><span class="sxs-lookup"><span data-stu-id="79653-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="79653-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79653-105">フォームライブラリには、フォームに関する重要な情報がすべて含まれます。フォームのプロパティ、動詞、およびサーバーの実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="79653-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="79653-106">クライアントによっては、フォームサーバーの保守、インストール、または削除をユーザーに許可することができます。</span><span class="sxs-lookup"><span data-stu-id="79653-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="79653-107">この機能をユーザーに提供するには、次のものにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="79653-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="79653-108">フォームサーバーの構成ファイル。このファイルには、が含まれます。CFG 拡張機能。</span><span class="sxs-lookup"><span data-stu-id="79653-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="79653-109">フォームライブラリの container オブジェクト[。 imapiformcontainer: IUnknown](imapiformcontaineriunknown.md)インターフェイスを実装するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="79653-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="79653-110">構成ファイルまたはパス名にアクセスするには、任意の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="79653-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="79653-111">通常、クライアントは、ユーザーに対してフォームサーバーをインストールおよび削除するためのダイアログボックスを表示します。このダイアログボックスを使用すると、構成ファイルの場所をユーザーに確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="79653-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="79653-112">フォームライブラリのコンテナーにアクセスするには、フォームマネージャーの[imapiformmgr:: openformcontainer](imapiformmgr-openformcontainer.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="79653-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="79653-113">開くフォームライブラリを指定する列挙値を渡し、必要に応じて、フォームマネージャーがフォームライブラリを開くために使用するオブジェクトへのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="79653-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="79653-114">たとえば、[フォルダーフォームライブラリ](folder-form-libraries.md)を開く場合は、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="79653-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="79653-115">**openformcontainer**が**imapiformcontainer**ポインターを返すと、実行するメンテナンスに応じて、 [imapiformcontainer:: installform](imapiformcontainer-installform.md)または[imapiformcontainer:: removeform](imapiformcontainer-removeform.md)のいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="79653-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="79653-116">**installform**は、フォームサーバーをライブラリに追加します。**removeform**ライブラリからフォームサーバーを削除します。</span><span class="sxs-lookup"><span data-stu-id="79653-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

