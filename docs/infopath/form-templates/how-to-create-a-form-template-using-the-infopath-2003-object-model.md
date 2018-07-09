---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2007, creating InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: このトピックの手順では、InfoPath 2003 互換オブジェクト モデルを操作するフォーム テンプレートの作成方法を説明します。
ms.openlocfilehash: 0cea526c2d41674afc6fee152c3e0584e6b69564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799114"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a><span data-ttu-id="6c7b4-104">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-104">Create a Form Template Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="6c7b4-105">このトピックの手順では、InfoPath 2003 互換オブジェクト モデルを操作するフォーム テンプレートの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-105">The procedures in this topic describe how to create a form template that works with the InfoPath 2003-compatible object model.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6c7b4-p101">以下の手順に加えて、[ **ファイル**] タブをクリックし、[ **名前を付けて保存**] をクリックして、[ **ファイルの種類**] ボックスで [ **InfoPath 2003 フォーム テンプレート**] を選択して、フォーム テンプレートを InfoPath 2003 互換ファイル形式で保存する必要があります。また、InfoPath で作成した InfoPath 2003 互換フォーム テンプレートを InfoPath 2003 ユーザーが開くには、コンピューターに .NET Framework 2.0 またはそれ以降がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-p101">In addition to the procedures below, you must also click the **File** tab, click **Save As**, and then select **InfoPath 2003 Form Template** in the **Save as type** box to save the form template to the InfoPath 2003-compatible file format. Also, to open InfoPath 2003-compatible form templates created with InfoPath, all InfoPath 2003 users must have the .NET Framework 2.0 or later installed on their computers.</span></span> 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a><span data-ttu-id="6c7b4-108">Visual Studio Tools for Applications がインストール済みの InfoPath で InfoPath 2003 互換フォーム テンプレートを作成するには</span><span class="sxs-lookup"><span data-stu-id="6c7b4-108">To create an InfoPath 2003-compatible form template in InfoPath with Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="6c7b4-109">InfoPath デザイン モードを起動します。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-109">Start the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="6c7b4-110">[ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-110">Click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="6c7b4-111">[ **互換性**] カテゴリで、[ **InfoPath 2003 エディター フォーム**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-111">In the **Compatibility** category, select **InfoPath 2003 Editor Form**.</span></span>
    
4. <span data-ttu-id="6c7b4-112">[ **プログラミング**] カテゴリで、[ **フォーム テンプレートのコード言語**] ボックスの一覧の [ **C# (InfoPath 2003 互換)**] または [ **Visual Basic (InfoPath 2003 互換)**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-112">In the **Programming** category, select either **C# (InfoPath 2003 Compatible)** or **Visual Basic (InfoPath 2003 Compatible)** from the **Form template code language** drop-down list.</span></span> 
    
5. <span data-ttu-id="6c7b4-113">[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-113">Click **OK**.</span></span>
    
6. <span data-ttu-id="6c7b4-114">フォーム テンプレートをデザインし[、イベント ハンドラーを使用して InfoPath 2003 オブジェクト モデルの追加](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)で説明するように Visual Studio 2012 でのイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="6c7b4-114">Design your form template, and then add event handlers in Visual Studio 2012, as described in [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c7b4-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c7b4-115">See also</span></span>



<span data-ttu-id="6c7b4-116">[[ウォークスルー] InfoPath 2003 オブジェクト モデルを使用して基本的なフォーム テンプレートを作成およびデバッグする方法](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="6c7b4-116">[Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)</span></span>
  
[<span data-ttu-id="6c7b4-117">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="6c7b4-117">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>](creating-form-templates-using-the-infopath-2003-object-model.md)

