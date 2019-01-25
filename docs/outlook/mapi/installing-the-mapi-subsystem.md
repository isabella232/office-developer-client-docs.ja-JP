---
title: MAPI サブシステムのインストール
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '最終更新日: 2015 年 3 月 9 日'
localization_priority: Priority
ms.openlocfilehash: 112a683f5967f8740c2d21285eb4ebbc0f455c48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722439"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="1c768-103">MAPI サブシステムのインストール</span><span class="sxs-lookup"><span data-stu-id="1c768-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="1c768-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c768-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c768-105">サポートされているバージョンの Windows で、_\<ドライブ\>_ \Windows\System32 フォルダーに MAPI スタブ ライブラリ、Mapi32.dll をインストールします。</span><span class="sxs-lookup"><span data-stu-id="1c768-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="1c768-106">サポートされているバージョンの Windows を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1c768-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="1c768-107">Windows 7。</span><span class="sxs-lookup"><span data-stu-id="1c768-107">Windows 7</span></span>
    
- <span data-ttu-id="1c768-108">Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="1c768-108">Windows Vista</span></span>
    
- <span data-ttu-id="1c768-109">Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="1c768-109">Windows Server 2008</span></span>
    
- <span data-ttu-id="1c768-110">Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="1c768-110">Windows Server 2003</span></span>
    
- <span data-ttu-id="1c768-111">Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1c768-111">Windows XP</span></span>
    
<span data-ttu-id="1c768-112">MAPI サブシステムを正しくインストールするには、MAPI ベースのサブシステム (Microsoft Outlook など) を含むアプリケーションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="1c768-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="1c768-113">コンピューターの MAPI サブシステムのインストールに関する情報は、システム レジストリにあります。</span><span class="sxs-lookup"><span data-stu-id="1c768-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="1c768-114">レジストリ エントリの値は、すべて文字列です。</span><span class="sxs-lookup"><span data-stu-id="1c768-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="1c768-115">メッセージ サービスのインストール プログラムは、次のシステム レジストリキーにインストール情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="1c768-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="1c768-116">メッセージ サービスは、システム レジストリにエントリを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c768-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="1c768-117">次の表に、クライアントがコンピューター上の MAPI サブシステムのバージョン情報を取得する方法を要約します。</span><span class="sxs-lookup"><span data-stu-id="1c768-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="1c768-118">**確認**</span><span class="sxs-lookup"><span data-stu-id="1c768-118">**To check**</span></span>|<span data-ttu-id="1c768-119">**レジストリ**</span><span class="sxs-lookup"><span data-stu-id="1c768-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c768-120">MAPI の可用性</span><span class="sxs-lookup"><span data-stu-id="1c768-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="1c768-121">`MAPIX=1` を検索します。</span><span class="sxs-lookup"><span data-stu-id="1c768-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="1c768-122">利用可能な MAPI のバージョン</span><span class="sxs-lookup"><span data-stu-id="1c768-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="1c768-123">" _x.x.x_" 形式の MAPIXVER 文字列を検索します。</span><span class="sxs-lookup"><span data-stu-id="1c768-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c768-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c768-124">See also</span></span>



[<span data-ttu-id="1c768-125">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="1c768-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

