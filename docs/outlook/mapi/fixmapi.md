---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800058"
---
# <a name="fixmapi"></a><span data-ttu-id="525a6-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="525a6-103">FixMAPI</span></span>

  
  
<span data-ttu-id="525a6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="525a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="525a6-105">によってバックアップ コピーが mapi32.dll のコピーの現在のクライアント コンピューター、および MAPI スタブ ライブラリのリストア mapi32.dll mapistub.dll。</span><span class="sxs-lookup"><span data-stu-id="525a6-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="525a6-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="525a6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="525a6-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="525a6-107">Exported by:</span></span>  <br/> |<span data-ttu-id="525a6-108">mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="525a6-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="525a6-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="525a6-109">Called by:</span></span>  <br/> |<span data-ttu-id="525a6-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="525a6-110">Client</span></span>  <br/> |
|<span data-ttu-id="525a6-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="525a6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="525a6-112">Windows</span><span class="sxs-lookup"><span data-stu-id="525a6-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="525a6-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="525a6-113">Return values</span></span>

<span data-ttu-id="525a6-114">関数が成功した場合は、0 以外の値を返します。</span><span class="sxs-lookup"><span data-stu-id="525a6-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="525a6-115">関数が失敗した場合は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="525a6-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="525a6-116">拡張エラー情報を取得するには、Microsoft Windows ソフトウェア開発キット (SDK) 関数、 **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="525a6-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="525a6-117">備考</span><span class="sxs-lookup"><span data-stu-id="525a6-117">Remarks</span></span>

 <span data-ttu-id="525a6-118">**FixMAPI**では、ファイルが読み取り専用としてマークされている場合、現在の mapi32.dll ファイルは置換されません。</span><span class="sxs-lookup"><span data-stu-id="525a6-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="525a6-119">**FixMAPI**では、Microsoft Exchange Server がコンピューターにインストールされている場合、現在の mapi32.dll は置換されません。</span><span class="sxs-lookup"><span data-stu-id="525a6-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="525a6-120">**FixMAPI**では、特定のコンピューター上の mapi32.dll のコピーの現在のバックアップ ・ コピーと [mapi32.dll] から別の名前がバックアップ ・ コピーで割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="525a6-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="525a6-121">バックアップ ・ コピーには、そのアセンブリの後続の呼び出しを指示します。</span><span class="sxs-lookup"><span data-stu-id="525a6-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="525a6-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="525a6-122">See also</span></span>



[<span data-ttu-id="525a6-123">KB 256946: Outlook 2000 を起動したときにプログラムの競合のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="525a6-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](http://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="525a6-124">KB 228457: Fixmapi.exe ツールの説明は、Internet Explorer 5 に含まれる</span><span class="sxs-lookup"><span data-stu-id="525a6-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](http://support.microsoft.com/kb/228457)

