---
title: MAPI サブシステムをインストールします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801070"
---
# <a name="installing-the-mapi-subsystem"></a><span data-ttu-id="0712a-103">MAPI サブシステムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="0712a-103">Installing the MAPI Subsystem</span></span>

  
  
<span data-ttu-id="0712a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0712a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0712a-105">サポートされているバージョンの Windows で Mapi32.dll、MAPI スタブ ライブラリをインストールする、_\<ドライブ\>_ \Windows\System32 フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="0712a-105">Supported versions of Windows install the MAPI stub library, Mapi32.dll, in the  _\<drive\>_ \Windows\System32 folder.</span></span> 
  
<span data-ttu-id="0712a-106">サポートされているバージョンの Windows は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0712a-106">The supported versions of Windows are as follows:</span></span>
  
- <span data-ttu-id="0712a-107">Windows 7。</span><span class="sxs-lookup"><span data-stu-id="0712a-107">Windows 7.</span></span>
    
- <span data-ttu-id="0712a-108">Windows Vista の場合です。</span><span class="sxs-lookup"><span data-stu-id="0712a-108">Windows Vista.</span></span>
    
- <span data-ttu-id="0712a-109">Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="0712a-109">Windows Server 2008.</span></span>
    
- <span data-ttu-id="0712a-110">Windows Server 2003 です。</span><span class="sxs-lookup"><span data-stu-id="0712a-110">Windows Server 2003.</span></span>
    
- <span data-ttu-id="0712a-111">Windows XP です。</span><span class="sxs-lookup"><span data-stu-id="0712a-111">Windows XP.</span></span>
    
<span data-ttu-id="0712a-112">MAPI のサブシステムを正しくインストールするには、Microsoft Outlook などの MAPI ベースのサブシステムを含むアプリケーションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="0712a-112">To correctly install the MAPI subsystem, install an application that contains a MAPI-based subsystem, such as Microsoft Outlook.</span></span>
  
<span data-ttu-id="0712a-113">システム レジストリで、コンピューターの MAPI サブシステムのインストールに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0712a-113">You can find information about a computer's MAPI subsystem installation in the system registry.</span></span> <span data-ttu-id="0712a-114">レジストリ エントリのすべての値は、文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="0712a-114">All values in the registry entries are character strings.</span></span> 
  
<span data-ttu-id="0712a-115">メッセージ サービスのインストール プログラムは、システムの次のレジストリ キーのインストール情報の作成を担当します。</span><span class="sxs-lookup"><span data-stu-id="0712a-115">Message service installation programs are responsible for creating the installation information in the following system registry key:</span></span> 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
<span data-ttu-id="0712a-116">メッセージ サービスは、システム レジストリにエントリを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0712a-116">Message services must add entries to the system registry.</span></span> 
  
<span data-ttu-id="0712a-117">次の表は、クライアントが自分のコンピューター上の MAPI サブシステムのバージョン情報を取得する方法をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="0712a-117">The following table summarizes how clients retrieve version information for the MAPI subsystem on their computer.</span></span>
  
|<span data-ttu-id="0712a-118">**チェックするには**</span><span class="sxs-lookup"><span data-stu-id="0712a-118">**To check**</span></span>|<span data-ttu-id="0712a-119">**Registry**</span><span class="sxs-lookup"><span data-stu-id="0712a-119">**Registry**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0712a-120">MAPI の可用性</span><span class="sxs-lookup"><span data-stu-id="0712a-120">Availability of MAPI</span></span>  <br/> |<span data-ttu-id="0712a-121">`MAPIX=1`。</span><span class="sxs-lookup"><span data-stu-id="0712a-121">Look for  `MAPIX=1`.</span></span>  <br/> |
|<span data-ttu-id="0712a-122">MAPI のバージョン</span><span class="sxs-lookup"><span data-stu-id="0712a-122">Available version of MAPI</span></span>  <br/> |<span data-ttu-id="0712a-123">" _X.x.x_"の形式の MAPIXVER 文字列を検索します。</span><span class="sxs-lookup"><span data-stu-id="0712a-123">Look for a MAPIXVER string of the form " _x.x.x_".</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0712a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="0712a-124">See also</span></span>



[<span data-ttu-id="0712a-125">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="0712a-125">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

