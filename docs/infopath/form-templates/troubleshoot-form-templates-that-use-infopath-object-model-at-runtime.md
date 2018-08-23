---
title: 実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティングを行う
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- troubleshooting form templates [infopath 2007], run time,InfoPath 2003-compatible form templates, troubleshooting at run time
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: ここでは、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間によって実行時に提供される InfoPath 2003 互換オブジェクト モデルを使用する、InfoPath マネージ コード フォーム テンプレートの操作時に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799222"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a><span data-ttu-id="86635-104">実行時に InfoPath オブジェクト モデルを使用するフォーム テンプレートのトラブルシューティングを行う</span><span class="sxs-lookup"><span data-stu-id="86635-104">Troubleshoot form templates that use the InfoPath object model at run time</span></span>

<span data-ttu-id="86635-105">ここでは、 **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって実行時に提供される InfoPath 2003 互換オブジェクト モデルを使用する、InfoPath マネージ コード フォーム テンプレートの操作時に発生する可能性のある一般的なトラブルシューティングのシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="86635-105">The following sections describe common troubleshooting scenarios you may encounter while working with InfoPath managed-code form templates that use the InfoPath 2003-compatible object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace at run time.</span></span> 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a><span data-ttu-id="86635-106">実行時にマネージ コードの未処理の例外の通知を表示します。</span><span class="sxs-lookup"><span data-stu-id="86635-106">Display notifications for unhandled managed-code exceptions at run time</span></span>

<span data-ttu-id="86635-107">フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="86635-107">If you do not use try-catch exception handling in your form code, InfoPath will display information about unhandled exceptions in the InfoPath error dialog box while debugging and previewing.</span></span> <span data-ttu-id="86635-108">しかし、既定では、マネージ コード フォーム テンプレートを展開した場合の実行時には、未処理の例外は Info Path エラー ダイアログ ボックスに表示されることはありません。</span><span class="sxs-lookup"><span data-stu-id="86635-108">However, by default, unhandled exceptions are not displayed in the InfoPath error dialog box at run time when you deploy your managed-code form template.</span></span> <span data-ttu-id="86635-109">マネージ コード例外の実行時に表示する場合は、[処理エラーを使用して InfoPath 2003 オブジェクト モデル](how-to-handle-errors-using-the-infopath-2003-object-model.md)の「マネージ コード例外の処理」セクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="86635-109">If you want managed-code exceptions displayed at run time, follow the procedure in the "Handling Managed Code Exceptions" section of [Handle Errors Using the InfoPath 2003 Object Model](how-to-handle-errors-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a><span data-ttu-id="86635-110">展開後のマネージ コードのフォーム テンプレートの問題</span><span class="sxs-lookup"><span data-stu-id="86635-110">Problems with managed-code form templates after deployment</span></span>

<span data-ttu-id="86635-111">マネージ コード フォーム テンプレートは、必ず最終的な展開先でテストしてください。</span><span class="sxs-lookup"><span data-stu-id="86635-111">Be sure to test your managed-code form template in the location where it will be finally deployed.</span></span> <span data-ttu-id="86635-112">展開手順については、[コードを含む InfoPath フォーム テンプレートの展開](how-to-deploy-infopath-form-templates-with-code.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86635-112">For information on deployment procedures, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="86635-113">展開に関係するセキュリティ シナリオの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86635-113">For information on security scenarios that affect deployment, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md).</span></span>
  
<span data-ttu-id="86635-114">.NET Framework 1.1 Configuration ユーティリティおよび InfoPath フォーム テンプレート コード グループを使用して、マネージ コード フォーム テンプレート専用のアクセス許可を追加する場合、同じセキュリティ ポリシーをすべてのクライアント コンピューターに展開してください。</span><span class="sxs-lookup"><span data-stu-id="86635-114">If you use the .NET Framework 1.1 Configuration utility and the InfoPath Form Templates code group to add specific permissions for a managed-code form template, make sure that the same security policy is deployed on all client computers.</span></span> <span data-ttu-id="86635-115">また、ローカル コンピューターの特定の場所を指す **URLEvidence** を指定する場合、指定先にはソリューションが最終的に展開されるフォルダー (展開中に使用される場所とは異なる場所) を指してください。</span><span class="sxs-lookup"><span data-stu-id="86635-115">Also, if you are specifying **URLEvidence** that refers to a location on the local computer, make sure that the specified location refers to the folder where the solution will be finally deployed (not the same location used during development).</span></span> <span data-ttu-id="86635-116">マネージ コード フォーム テンプレートの.NET Framework のセキュリティの設定を構成する方法の詳細については、[コードのフォーム テンプレートのセキュリティ設定の構成](how-to-configure-security-settings-for-form-templates-with-code.md)のトピックの「を割り当てること FullTrust をフォームで特定の URL または UNC」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86635-116">For information on configuring .NET Framework security settings for a managed-code form template, see the "Assigning FullTrust to Forms at a Specific URL or UNC" section of the [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md) topic.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86635-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="86635-117">See also</span></span>

- [<span data-ttu-id="86635-118">コードを含むフォーム テンプレートのためのセキュリティ モデルについて</span><span class="sxs-lookup"><span data-stu-id="86635-118">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)
- [<span data-ttu-id="86635-119">コードを含む InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="86635-119">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
- [<span data-ttu-id="86635-120">InfoPath 2003 オブジェクト モデルを使用してエラーを処理する</span><span class="sxs-lookup"><span data-stu-id="86635-120">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [<span data-ttu-id="86635-121">InfoPath 2003 オブジェクト モデルを使用して InfoPath プロジェクトをデバッグする</span><span class="sxs-lookup"><span data-stu-id="86635-121">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

