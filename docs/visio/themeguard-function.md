---
title: THEMEGUARD 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: 図形の書式設定セルを保護して、現在のテーマの適切な側面を使用していることを確認します。
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326755"
---
# <a name="themeguard-function"></a><span data-ttu-id="e39c5-103">THEMEGUARD 関数</span><span class="sxs-lookup"><span data-stu-id="e39c5-103">THEMEGUARD Function</span></span>

<span data-ttu-id="e39c5-104">図形の書式設定セルを保護して、現在のテーマの適切な側面を使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e39c5-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e39c5-105">構文</span><span class="sxs-lookup"><span data-stu-id="e39c5-105">Syntax</span></span>

<span data-ttu-id="e39c5-106">THEMEGUARD ()</span><span class="sxs-lookup"><span data-stu-id="e39c5-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e39c5-107">解説</span><span class="sxs-lookup"><span data-stu-id="e39c5-107">Remarks</span></span>

<span data-ttu-id="e39c5-108">THEMEGUARD 関数をセルに適用しても、GUARD 関数の場合と同様、手動でフォーマットを適用することは可能です。</span><span class="sxs-lookup"><span data-stu-id="e39c5-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="e39c5-109">ユーザーインターフェイスの図形に書式を適用した場合、またはオートメーションを使用して、手動で書式設定する値を格納するために SETATREFEXPR 関数を数式に含める場合を除き、THEMEGUARD 数式は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e39c5-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e39c5-110">例</span><span class="sxs-lookup"><span data-stu-id="e39c5-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="e39c5-111">主テーマに設定された塗りつぶし色の代わりに、現在のテーマの Accent 2 の色で図形を塗りつぶすよう指定します。</span><span class="sxs-lookup"><span data-stu-id="e39c5-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

