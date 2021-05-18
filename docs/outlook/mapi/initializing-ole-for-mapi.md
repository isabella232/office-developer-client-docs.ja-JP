---
title: OLE for MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317228"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="43a98-103">OLE for MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="43a98-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="43a98-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43a98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43a98-105">OLE も使用する場合は、OLE 関数 [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) を呼び出して OLE ライブラリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="43a98-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="43a98-106">**OleInitialize は** 、セッションのグローバル データを初期化し、呼び出しを受け入れる OLE ライブラリを準備します。</span><span class="sxs-lookup"><span data-stu-id="43a98-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="43a98-107">**OleInitialize の呼び出しの詳細については、SDK** のWindowsしてください。</span><span class="sxs-lookup"><span data-stu-id="43a98-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

