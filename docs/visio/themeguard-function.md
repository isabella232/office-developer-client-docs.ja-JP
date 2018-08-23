---
title: THEMEGUARD 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: 現在のテーマの適切な設定を使用するようにするのには図形のセルの書式設定を保護します。
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806642"
---
# <a name="themeguard-function"></a><span data-ttu-id="60345-103">THEMEGUARD 関数</span><span class="sxs-lookup"><span data-stu-id="60345-103">THEMEGUARD Function</span></span>

<span data-ttu-id="60345-104">現在のテーマの適切な設定を使用するようにするのには図形のセルの書式設定を保護します。</span><span class="sxs-lookup"><span data-stu-id="60345-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="60345-105">構文</span><span class="sxs-lookup"><span data-stu-id="60345-105">Syntax</span></span>

<span data-ttu-id="60345-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="60345-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60345-107">注釈</span><span class="sxs-lookup"><span data-stu-id="60345-107">Remarks</span></span>

<span data-ttu-id="60345-108">THEMEGUARD 関数をセルに適用すること防ぐことはできませんが、ガードを適用する関数と同じ方法で手動で書式設定をします。</span><span class="sxs-lookup"><span data-stu-id="60345-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="60345-109">ユーザー インターフェイスまたはオートメーションを使用してプログラムを使用して、図形を書式設定する場合、THEMEGUARD 式をオーバーライドすると、手動の書式設定の値を格納する数式に、SETATREFEXPR 関数を追加する場合を除き、します。</span><span class="sxs-lookup"><span data-stu-id="60345-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="60345-110">例</span><span class="sxs-lookup"><span data-stu-id="60345-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="60345-111">主テーマに設定された塗りつぶし色の代わりに、現在のテーマの Accent 2 の色で図形を塗りつぶすよう指定します。</span><span class="sxs-lookup"><span data-stu-id="60345-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

