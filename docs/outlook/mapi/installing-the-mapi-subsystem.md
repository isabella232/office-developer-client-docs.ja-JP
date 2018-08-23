---
title: MAPI サブシステムのインストール
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: adb4d09ccce95683ac46e7b271fafa328b1a9f97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575351"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="c1caf-103">MAPI サブシステムのインストール</span><span class="sxs-lookup"><span data-stu-id="c1caf-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="c1caf-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1caf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1caf-105">サポートされているバージョンの Windows で Mapi32.dll、MAPI スタブ ライブラリをインストールする、_\<ドライブ\>_ \Windows\System32 フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="c1caf-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="c1caf-106">サポートされているバージョンの Windows は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c1caf-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="c1caf-107">Windows 7。</span><span class="sxs-lookup"><span data-stu-id="c1caf-107">Windows 7.</span></span>
    
- <span data-ttu-id="c1caf-108">Windows Vista の場合です。</span><span class="sxs-lookup"><span data-stu-id="c1caf-108">Windows Vista.</span></span>
    
- <span data-ttu-id="c1caf-109">Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="c1caf-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="c1caf-110">Windows Server 2003 です。</span><span class="sxs-lookup"><span data-stu-id="c1caf-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="c1caf-111">Windows XP です。</span><span class="sxs-lookup"><span data-stu-id="c1caf-111">Windows XP.</span></span>
    
<span data-ttu-id="c1caf-112">MAPI のサブシステムを正しくインストールするには、Microsoft Outlook などの MAPI ベースのサブシステムを含むアプリケーションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="c1caf-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="c1caf-113">システム レジストリで、コンピューターの MAPI サブシステムのインストールに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1caf-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="c1caf-114">レジストリ エントリのすべての値は、文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c1caf-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="c1caf-115">メッセージ サービスのインストール プログラムは、システムの次のレジストリ キーのインストール情報の作成を担当します。</span><span class="sxs-lookup"><span data-stu-id="c1caf-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="c1caf-116">メッセージ サービスは、システム レジストリにエントリを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1caf-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="c1caf-117">次の表は、クライアントが自分のコンピューター上の MAPI サブシステムのバージョン情報を取得する方法をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="c1caf-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="c1caf-118">**チェックするには**</span><span class="sxs-lookup"><span data-stu-id="c1caf-118">**To check**</span></span>|<span data-ttu-id="c1caf-119">**Registry**</span><span class="sxs-lookup"><span data-stu-id="c1caf-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1caf-120">MAPI の可用性</span><span class="sxs-lookup"><span data-stu-id="c1caf-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="c1caf-121">`MAPIX=1`。</span><span class="sxs-lookup"><span data-stu-id="c1caf-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="c1caf-122">MAPI のバージョン</span><span class="sxs-lookup"><span data-stu-id="c1caf-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="c1caf-123">" _X.x.x_"の形式の MAPIXVER 文字列を検索します。</span><span class="sxs-lookup"><span data-stu-id="c1caf-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1caf-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1caf-124">See also</span></span>



[<span data-ttu-id="c1caf-125">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="c1caf-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

