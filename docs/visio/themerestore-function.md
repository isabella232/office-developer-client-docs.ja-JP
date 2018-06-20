---
title: THEMERESTORE 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: 場合に復元できるローカルの書式設定、ユーザーが後でテーマを削除するためにテーマを適用するときは、図形のローカル書式設定の値を格納します。
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806655"
---
# <a name="themerestore-function"></a><span data-ttu-id="81790-103">THEMERESTORE 関数</span><span class="sxs-lookup"><span data-stu-id="81790-103">THEMERESTORE Function</span></span>

<span data-ttu-id="81790-104">場合に復元できるローカルの書式設定、ユーザーが後でテーマを削除するためにテーマを適用するときは、図形のローカル書式設定の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="81790-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="81790-105">構文</span><span class="sxs-lookup"><span data-stu-id="81790-105">Syntax</span></span>

<span data-ttu-id="81790-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="81790-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="81790-107">例</span><span class="sxs-lookup"><span data-stu-id="81790-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="81790-108">現在のテーマを削除するときに、以前図形に適用された個別の塗りつぶしの色書式を復元します。</span><span class="sxs-lookup"><span data-stu-id="81790-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

