---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334962"
---
# <a name="fixmapi"></a><span data-ttu-id="ff21d-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="ff21d-103">FixMAPI</span></span>

  
  
<span data-ttu-id="ff21d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff21d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff21d-105">クライアントコンピューターに mapi32 の現在のコピーのバックアップコピーを作成し、mapi32 を MAPI スタブライブラリ mapistub に復元して復元します。</span><span class="sxs-lookup"><span data-stu-id="ff21d-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff21d-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ff21d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff21d-107">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="ff21d-107">Exported by:</span></span>  <br/> |<span data-ttu-id="ff21d-108">mapistub</span><span class="sxs-lookup"><span data-stu-id="ff21d-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="ff21d-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ff21d-109">Called by:</span></span>  <br/> |<span data-ttu-id="ff21d-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="ff21d-110">Client</span></span>  <br/> |
|<span data-ttu-id="ff21d-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="ff21d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff21d-112">Windows</span><span class="sxs-lookup"><span data-stu-id="ff21d-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="ff21d-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="ff21d-113">Return values</span></span>

<span data-ttu-id="ff21d-114">関数が正常に終了した場合、戻り値は0以外の値になります。</span><span class="sxs-lookup"><span data-stu-id="ff21d-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="ff21d-115">関数が失敗した場合、戻り値は0になります。</span><span class="sxs-lookup"><span data-stu-id="ff21d-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ff21d-116">拡張エラー情報を取得するには、Microsoft Windows Software Development Kit (SDK) 関数 ( **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ff21d-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff21d-117">解説</span><span class="sxs-lookup"><span data-stu-id="ff21d-117">Remarks</span></span>

 <span data-ttu-id="ff21d-118">**FixMAPI**は、ファイルが読み取り専用としてマークされている場合は、現在の mapi32 ファイルを置き換えません。</span><span class="sxs-lookup"><span data-stu-id="ff21d-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="ff21d-119">**FixMAPI**は、Microsoft Exchange Server がコンピューターにインストールされている場合は、現在の mapi32 を置き換えません。</span><span class="sxs-lookup"><span data-stu-id="ff21d-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="ff21d-120">**FixMAPI**がコンピューターに mapi32 の現在のコピーのバックアップコピーを作成すると、"mapi32" とは異なる名前がバックアップコピーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="ff21d-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="ff21d-121">その後、そのアセンブリに対する後続の呼び出しがバックアップコピーに送られます。</span><span class="sxs-lookup"><span data-stu-id="ff21d-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff21d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff21d-122">See also</span></span>



[<span data-ttu-id="ff21d-123">KB 256946: Outlook 2000 の起動時にプログラムの競合エラーメッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="ff21d-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="ff21d-124">KB 228457: Internet Explorer 5 に含まれる Fixmapi ツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ff21d-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

