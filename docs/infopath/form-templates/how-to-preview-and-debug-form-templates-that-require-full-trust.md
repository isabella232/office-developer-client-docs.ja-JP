---
title: 完全な信頼が必要なフォーム テンプレートをプレビューおよびデバッグする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: 既定では、完全な信頼が必要なオブジェクト モデルのメンバーを起動するコードを含むマネージ コード プロジェクト (ユーザーのログイン ドメインに関する情報へのアクセスを必要とする LoginName プロパティなど) をデバッグまたはプレビューしようとすると、Microsoft InfoPath では次のようになります。
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411261"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="6b56b-104">完全な信頼が必要なフォーム テンプレートをプレビューおよびデバッグする</span><span class="sxs-lookup"><span data-stu-id="6b56b-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="6b56b-105">既定では、完全な信頼が必要なオブジェクト モデルのメンバーを起動するコードを含むマネージ コード プロジェクト (ユーザーのログイン ドメインに関する情報へのアクセスを必要とする **LoginName** プロパティなど) をデバッグまたはプレビューしようとすると、Microsoft InfoPath では次のようになります。</span><span class="sxs-lookup"><span data-stu-id="6b56b-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="6b56b-106">プレビュー時 :</span><span class="sxs-lookup"><span data-stu-id="6b56b-106">When previewing:</span></span>
  
<span data-ttu-id="6b56b-p101">"ハンドルされていない例外がフォームのコードで発生しました" に続いて "フォームのコードにエラーが含まれるため、この操作を完了できませんでした" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b56b-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="6b56b-109">デバッグ時 :</span><span class="sxs-lookup"><span data-stu-id="6b56b-109">When debugging:</span></span>
  
<span data-ttu-id="6b56b-110">コード エディターで、完全な信頼が必要なメンバーを呼び出しているコード行にフォーカスが移動し、" **SecurityException** はユーザー コードによってハンドルされませんでした。要求が失敗しました" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b56b-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="6b56b-111">デバッグ時またはプレビュー時に、フォーム テンプレートのビジネス ロジックがこのメンバーを呼び出すことを許可するには、前の手順に示したように、フォーム テンプレートのセキュリティ レベルを [ **完全信頼**] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b56b-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="6b56b-112">完全な信頼が必要なマネージ コード フォーム テンプレートを構成する</span><span class="sxs-lookup"><span data-stu-id="6b56b-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="6b56b-113">フォームのセキュリティ レベルを完全信頼に設定する</span><span class="sxs-lookup"><span data-stu-id="6b56b-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="6b56b-114">InfoPath のデザイン モードでフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b56b-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="6b56b-115">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b56b-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="6b56b-116">[ **カテゴリ**] ボックスの一覧の [ **セキュリティと信頼**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b56b-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="6b56b-117">[ **セキュリティ レベル**] の [ **自動的にセキュリティ レベルを設定する**] をオフにします。</span><span class="sxs-lookup"><span data-stu-id="6b56b-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="6b56b-118">**[完全信頼]** を選択してから、**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b56b-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="6b56b-119">この手順を実行すると、「[コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-infopath-form-templates-with-code.md)」の説明に従ってプロジェクトをデバッグできるようになります。</span><span class="sxs-lookup"><span data-stu-id="6b56b-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="6b56b-120">完全信頼を必要とするマネージ コード フォーム テンプレートを正しく展開するには、フォーム テンプレートのデジタル署名、インストールと登録などの追加の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="6b56b-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="6b56b-121">デバッグ後のマネージ コード フォーム テンプレートの展開方法については、「[コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b56b-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b56b-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b56b-122">See also</span></span>



[<span data-ttu-id="6b56b-123">コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする</span><span class="sxs-lookup"><span data-stu-id="6b56b-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="6b56b-124">コードを含む InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="6b56b-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

