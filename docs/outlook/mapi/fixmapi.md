---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334962"
---
# <a name="fixmapi"></a><span data-ttu-id="a6d77-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="a6d77-103">FixMAPI</span></span>

  
  
<span data-ttu-id="a6d77-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6d77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6d77-105">クライアント コンピューター上の現在のコピーのmapi32.dllコピーを作成し、MAPI スタブ ライブラリを使用mapi32.dllを復元します。mapistub.dll。</span><span class="sxs-lookup"><span data-stu-id="a6d77-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a6d77-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a6d77-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6d77-107">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="a6d77-107">Exported by:</span></span>  <br/> |<span data-ttu-id="a6d77-108">mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="a6d77-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="a6d77-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a6d77-109">Called by:</span></span>  <br/> |<span data-ttu-id="a6d77-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="a6d77-110">Client</span></span>  <br/> |
|<span data-ttu-id="a6d77-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="a6d77-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6d77-112">Windows</span><span class="sxs-lookup"><span data-stu-id="a6d77-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="a6d77-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="a6d77-113">Return values</span></span>

<span data-ttu-id="a6d77-114">関数が成功した場合、戻り値は 0 以外の値になります。</span><span class="sxs-lookup"><span data-stu-id="a6d77-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="a6d77-115">関数が失敗した場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="a6d77-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="a6d77-116">拡張エラー情報を取得するには、Microsoft Windows ソフトウェア開発キット (SDK) 関数 **[GetLastError を呼び出します](https://msdn.microsoft.com/library/ms679360.aspx)**。</span><span class="sxs-lookup"><span data-stu-id="a6d77-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6d77-117">注釈</span><span class="sxs-lookup"><span data-stu-id="a6d77-117">Remarks</span></span>

 <span data-ttu-id="a6d77-118">**ファイルが読み** 取り専用としてマークされている場合、FixMAPI は現在mapi32.dllファイルを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6d77-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="a6d77-119">**FixMAPI** は、コンピューターにインストールされているmapi32.dll現在Microsoft Exchange Server置き換えるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="a6d77-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="a6d77-120">**FixMAPI** がコンピューター上の mapi32.dll の現在のコピーのバックアップ コピーを作成すると、バックアップ コピーに "mapi32.dll" とは異なる名前が割り当mapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="a6d77-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="a6d77-121">その後、そのアセンブリを対象とした後続の呼び出しをバックアップ コピーに指示します。</span><span class="sxs-lookup"><span data-stu-id="a6d77-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6d77-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6d77-122">See also</span></span>



[<span data-ttu-id="a6d77-123">KB 256946: 2000 から開始すると、プログラムの競合Outlookされます。</span><span class="sxs-lookup"><span data-stu-id="a6d77-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="a6d77-124">KB 228457: 5 に付属Fixmapi.exeツールのInternet Explorer説明</span><span class="sxs-lookup"><span data-stu-id="a6d77-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

