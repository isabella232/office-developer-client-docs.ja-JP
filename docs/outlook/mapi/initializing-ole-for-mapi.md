---
title: OLE for MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589806"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="3b952-103">OLE for MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="3b952-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="3b952-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b952-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b952-105">OLE を使用する場合は、OLE ライブラリの初期化には、 [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)の OLE 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b952-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="3b952-106">**OleInitialize**は、セッションのグローバル データを初期化し、OLE ライブラリ呼び出しを受け入れるための準備を行います。</span><span class="sxs-lookup"><span data-stu-id="3b952-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="3b952-107">**OleInitialize**呼び出しの詳細については、Windows SDK を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b952-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

