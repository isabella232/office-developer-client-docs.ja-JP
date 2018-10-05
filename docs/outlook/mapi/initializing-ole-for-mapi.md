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
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388417"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="40e13-103">OLE for MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="40e13-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="40e13-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40e13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40e13-105">OLE を使用する場合は、OLE ライブラリの初期化には、 [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の OLE 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="40e13-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="40e13-106">**OleInitialize**は、セッションのグローバル データを初期化し、OLE ライブラリ呼び出しを受け入れるための準備を行います。</span><span class="sxs-lookup"><span data-stu-id="40e13-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="40e13-107">**OleInitialize**呼び出しの詳細については、Windows SDK を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40e13-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

