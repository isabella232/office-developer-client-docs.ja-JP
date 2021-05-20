---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog function [excel 2007],fDialog12 function [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431527"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="f5b8a-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="f5b8a-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="f5b8a-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f5b8a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f5b8a-p101">ユーザー定義コマンドの例で、C API のダイアログ ボックスの機能を使用して、DLL 内で Microsoft Excel UDD (ユーザー定義のダイアログ ボックス) を作成する方法を説明します。GENERIC.xll が読み込まれると、このコマンドにアクセスするのに使用するユーザー定義メニュー [Generic] を作成します。</span><span class="sxs-lookup"><span data-stu-id="f5b8a-p101">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="f5b8a-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5b8a-108">Parameters</span></span>

<span data-ttu-id="f5b8a-109">この関数にはパラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="f5b8a-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f5b8a-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="f5b8a-110">Property value/Return value</span></span>

<span data-ttu-id="f5b8a-111">この関数は、常に 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="f5b8a-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="f5b8a-112">例</span><span class="sxs-lookup"><span data-stu-id="f5b8a-112">Example</span></span>

<span data-ttu-id="f5b8a-113">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5b8a-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5b8a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5b8a-114">See also</span></span>



[<span data-ttu-id="f5b8a-115">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="f5b8a-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

