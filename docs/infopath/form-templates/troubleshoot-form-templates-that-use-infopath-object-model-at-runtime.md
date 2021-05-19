---
title: 実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- フォーム テンプレートのトラブルシューティング [infopath 2007]、実行時、InfoPath 2003 互換フォーム テンプレート、実行時のトラブルシューティング
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: 次のセクションでは、Microsoft が提供する InfoPath 2003 互換オブジェクト モデルを使用する InfoPath マネージ コード フォーム テンプレートの操作中に発生する可能性のある一般的なトラブルシューティングシナリオについて説明します。Office.Interop.InfoPath.SemiTrust 名前空間を実行時に指定します。
ms.openlocfilehash: c7b4b65cc722e72ef155529a0b2aa66c4f6cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414446"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a><span data-ttu-id="498de-104">実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="498de-104">Troubleshoot form templates that use the InfoPath object model at run time</span></span>

<span data-ttu-id="498de-105">以下のセクションでは、実行時に **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供される InfoPath 2003 互換オブジェクト モデルを使用する InfoPath マネージ コード フォーム テンプレートを操作する際に発生する一般的なトラブルシューティングシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="498de-105">The following sections describe common troubleshooting scenarios you may encounter while working with InfoPath managed-code form templates that use the InfoPath 2003-compatible object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace at run time.</span></span> 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a><span data-ttu-id="498de-106">実行時に未処理のマネージ コード例外の通知を表示する</span><span class="sxs-lookup"><span data-stu-id="498de-106">Display notifications for unhandled managed-code exceptions at run time</span></span>

<span data-ttu-id="498de-107">フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="498de-107">If you do not use try-catch exception handling in your form code, InfoPath will display information about unhandled exceptions in the InfoPath error dialog box while debugging and previewing.</span></span> <span data-ttu-id="498de-108">しかし、既定では、マネージ コード フォーム テンプレートを展開した場合の実行時には、未処理の例外は Info Path エラー ダイアログ ボックスに表示されることはありません。</span><span class="sxs-lookup"><span data-stu-id="498de-108">However, by default, unhandled exceptions are not displayed in the InfoPath error dialog box at run time when you deploy your managed-code form template.</span></span> <span data-ttu-id="498de-109">実行時にマネージ コード例外を表示する場合は [、「InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用したエラーの処理」の「マネージ コード例外の処理」セクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="498de-109">If you want managed-code exceptions displayed at run time, follow the procedure in the "Handling Managed Code Exceptions" section of [Handle Errors Using the InfoPath 2003 Object Model](how-to-handle-errors-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a><span data-ttu-id="498de-110">展開後のマネージ コード フォーム テンプレートの問題</span><span class="sxs-lookup"><span data-stu-id="498de-110">Problems with managed-code form templates after deployment</span></span>

<span data-ttu-id="498de-111">マネージ コード フォーム テンプレートは、必ず最終的な展開先でテストしてください。</span><span class="sxs-lookup"><span data-stu-id="498de-111">Be sure to test your managed-code form template in the location where it will be finally deployed.</span></span> <span data-ttu-id="498de-112">展開手順の詳細については、「コードを使用して [InfoPath フォーム テンプレートを展開する」を参照してください](how-to-deploy-infopath-form-templates-with-code.md)。</span><span class="sxs-lookup"><span data-stu-id="498de-112">For information on deployment procedures, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="498de-113">展開に影響するセキュリティ シナリオの詳細については、「コードを使用したフォーム テンプレートのセキュリティ モデルについて [」を参照してください](about-the-security-model-for-form-templates-with-code.md)。</span><span class="sxs-lookup"><span data-stu-id="498de-113">For information on security scenarios that affect deployment, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md).</span></span>
  
<span data-ttu-id="498de-114">.NET Framework 1.1 Configuration ユーティリティおよび InfoPath フォーム テンプレート コード グループを使用して、マネージ コード フォーム テンプレート専用のアクセス許可を追加する場合、同じセキュリティ ポリシーをすべてのクライアント コンピューターに展開してください。</span><span class="sxs-lookup"><span data-stu-id="498de-114">If you use the .NET Framework 1.1 Configuration utility and the InfoPath Form Templates code group to add specific permissions for a managed-code form template, make sure that the same security policy is deployed on all client computers.</span></span> <span data-ttu-id="498de-115">また、ローカル コンピューターの特定の場所を指す **URLEvidence** を指定する場合、指定先にはソリューションが最終的に展開されるフォルダー (展開中に使用される場所とは異なる場所) を指してください。</span><span class="sxs-lookup"><span data-stu-id="498de-115">Also, if you are specifying **URLEvidence** that refers to a location on the local computer, make sure that the specified location refers to the folder where the solution will be finally deployed (not the same location used during development).</span></span> <span data-ttu-id="498de-116">マネージ コード フォーム テンプレートの .NET Framework セキュリティ設定の構成の詳細については、「Configure Security 設定 for Form [Templates](how-to-configure-security-settings-for-form-templates-with-code.md) with Code」の「特定の URL または UNC でのフォームへのフルトラストの割り当て」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="498de-116">For information on configuring .NET Framework security settings for a managed-code form template, see the "Assigning FullTrust to Forms at a Specific URL or UNC" section of the [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md) topic.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="498de-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="498de-117">See also</span></span>

- [<span data-ttu-id="498de-118">コードを含むフォーム テンプレートのためのセキュリティ モデルについて</span><span class="sxs-lookup"><span data-stu-id="498de-118">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)
- [<span data-ttu-id="498de-119">コードを含む InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="498de-119">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
- [<span data-ttu-id="498de-120">InfoPath 2003 オブジェクト モデルを使用してエラーを処理する</span><span class="sxs-lookup"><span data-stu-id="498de-120">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [<span data-ttu-id="498de-121">InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする</span><span class="sxs-lookup"><span data-stu-id="498de-121">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

