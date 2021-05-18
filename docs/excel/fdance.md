---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance function [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409049"
---
# <a name="fdance"></a><span data-ttu-id="6fb2a-104">fDance</span><span class="sxs-lookup"><span data-stu-id="6fb2a-104">fDance</span></span>

 <span data-ttu-id="6fb2a-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6fb2a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6fb2a-p101">ユーザーが **[Esc]** を押すまで、作業中のワークシートの選択セルを変更するサンプル ユーザー定義コマンド。GENERIC.xll が読み込まれると、このコマンドにアクセスするためのユーザー定義メニュー [Generic] を作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-p101">Example user-defined command that changes the selected cells on the active worksheet around until the user presses **ESC**. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a><span data-ttu-id="6fb2a-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6fb2a-108">Parameters</span></span>

<span data-ttu-id="6fb2a-109">この関数にはパラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6fb2a-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="6fb2a-110">Property value/Return value</span></span>

<span data-ttu-id="6fb2a-111">この関数は、常に 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6fb2a-112">注釈</span><span class="sxs-lookup"><span data-stu-id="6fb2a-112">Remarks</span></span>

<span data-ttu-id="6fb2a-p102">これは、時間のかかる操作の例です。関数 [xlAbort](xlabort.md) を呼び出すこともあります。これは (協調的マルチタスキングを支援する) プロセッサを生成し、ユーザーが **[Esc]** を押して操作を取り消したかどうかを確認します。ボタンが押された場合は、ユーザーが中止操作をキャンセルできるようにします。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-p102">This is an example of a lengthy operation. It calls the function [xlAbort](xlabort.md) occasionally. This yields the processor (helping with cooperative multitasking), and checks whether the user has pressed **ESC** to cancel the operation. If so, it offers the user a chance to cancel the abort.</span></span> 
  
### <a name="example"></a><span data-ttu-id="6fb2a-117">例</span><span class="sxs-lookup"><span data-stu-id="6fb2a-117">Example</span></span>

<span data-ttu-id="6fb2a-118">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fb2a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="6fb2a-119">See also</span></span>



[<span data-ttu-id="6fb2a-120">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="6fb2a-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

