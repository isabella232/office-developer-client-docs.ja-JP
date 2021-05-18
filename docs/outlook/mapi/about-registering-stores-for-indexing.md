---
title: 概要 - インデックス作成用のストアの登録
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321827"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="13809-103">概要 - インデックス作成用のストアの登録</span><span class="sxs-lookup"><span data-stu-id="13809-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="13809-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13809-105">このトピックは、2007 年のインスタント検索Microsoft Office Outlookです。</span><span class="sxs-lookup"><span data-stu-id="13809-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="13809-106">インスタント検索を使用すると、アプリ内のアイテムをすばやくOutlook。</span><span class="sxs-lookup"><span data-stu-id="13809-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="13809-107">デスクトップ検索のコンポーネントWindows使用します。</span><span class="sxs-lookup"><span data-stu-id="13809-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="13809-108">MAPI プロトコル ハンドラーは、検索Windowsインデックスを作成する必要があるストアのレジストリをチェックします。</span><span class="sxs-lookup"><span data-stu-id="13809-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="13809-109">インデックスを作成するストア プロバイダーは、レジストリに登録Windows必要があります。</span><span class="sxs-lookup"><span data-stu-id="13809-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="13809-110">既定では、Windowsデスクトップ検索は、インデックス作成を許可するために、次の 4 種類のストア プロバイダーを Windowsレジストリに追加します。</span><span class="sxs-lookup"><span data-stu-id="13809-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="13809-111">個人用フォルダー ファイルの保存 (.PST)。</span><span class="sxs-lookup"><span data-stu-id="13809-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="13809-112">Microsoft Exchange(オフライン フォルダー ファイル (.ost) を含む) を格納します。</span><span class="sxs-lookup"><span data-stu-id="13809-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="13809-113">パブリック フォルダー用のストア。</span><span class="sxs-lookup"><span data-stu-id="13809-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="13809-114">MSN 用Microsoft Office Outlookコネクタ用に格納します。</span><span class="sxs-lookup"><span data-stu-id="13809-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="13809-115">インデックスを作成するサード パーティのストア プロバイダーは、自身をレジストリに登録Windows必要があります。</span><span class="sxs-lookup"><span data-stu-id="13809-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="13809-116">管理者とユーザーは、グループ ポリシー設定を使用して、デスクトップWindowsアイテムのインデックスを作成Outlookできます。</span><span class="sxs-lookup"><span data-stu-id="13809-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="13809-117">詳細については[、「Extending Windows デスクトップ検索」を参照してください](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="13809-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="13809-118">レジストリ キー</span><span class="sxs-lookup"><span data-stu-id="13809-118">Registry Keys</span></span>

<span data-ttu-id="13809-119">コンピューターでは、インデックスを作成するストア プロバイダーはすべて、次の 3 つのレジストリ キーの 1 つのみ登録する必要があります。Windowsします。</span><span class="sxs-lookup"><span data-stu-id="13809-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="13809-120">MAPI プロトコル ハンドラーは、これらの各キーの下を次の順序で確認します。</span><span class="sxs-lookup"><span data-stu-id="13809-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="13809-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span><span class="sxs-lookup"><span data-stu-id="13809-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span></span>\
    
2. <span data-ttu-id="13809-122">[HKLM]\Software\Microsoft\Windows\Windows\Preferences</span><span class="sxs-lookup"><span data-stu-id="13809-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
3. <span data-ttu-id="13809-123">[HKCU]\Software\Microsoft\Windows\Windows\Preferences</span><span class="sxs-lookup"><span data-stu-id="13809-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
 <span data-ttu-id="13809-124">キーの下の各値は、インデックスが作成されるストア プロバイダーに対応します。</span><span class="sxs-lookup"><span data-stu-id="13809-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="13809-125">値の名前は、ストア プロバイダーのグローバル一意識別子 (GUID) です。これは **DWORD** 型で、値は 16 進値0x00000001。</span><span class="sxs-lookup"><span data-stu-id="13809-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="13809-126">ストア プロバイダーの GUID</span><span class="sxs-lookup"><span data-stu-id="13809-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="13809-127">MAPI プロパティは **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** MAPI ストアの GUID を指定します。</span><span class="sxs-lookup"><span data-stu-id="13809-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="13809-128">インデックスを作成するストア プロバイダー Outlook、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="13809-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="13809-129">**ストア プロバイダーの種類**</span><span class="sxs-lookup"><span data-stu-id="13809-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="13809-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="13809-130">**GUID**</span></span> <br/> |<span data-ttu-id="13809-131">**注**</span><span class="sxs-lookup"><span data-stu-id="13809-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="13809-132">個人用フォルダー ファイル (.PST)</span><span class="sxs-lookup"><span data-stu-id="13809-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="13809-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="13809-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="13809-134">GUID は、パブリック ヘッダー ファイル mspst.h に次のように **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="13809-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="13809-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="13809-135">Exchange</span></span>  <br/> |<span data-ttu-id="13809-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="13809-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="13809-137">GUID はパブリック ヘッダー ファイル edkmdb.h に **pbExchangeProviderPrimaryUserGuid として文書化されています**</span><span class="sxs-lookup"><span data-stu-id="13809-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="13809-138">パブリック フォルダー</span><span class="sxs-lookup"><span data-stu-id="13809-138">Public folders</span></span>  <br/> |<span data-ttu-id="13809-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="13809-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="13809-140">GUID はパブリック ヘッダー ファイル edkmdb.h に **pbExchangeProviderPublicGuid として文書化されています**</span><span class="sxs-lookup"><span data-stu-id="13809-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="13809-141">OutlookMSN 用コネクタ</span><span class="sxs-lookup"><span data-stu-id="13809-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="13809-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="13809-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="13809-143">なし</span><span class="sxs-lookup"><span data-stu-id="13809-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13809-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="13809-144">See also</span></span>



[<span data-ttu-id="13809-145">ストア API について</span><span class="sxs-lookup"><span data-stu-id="13809-145">About the Store API</span></span>](about-the-store-api.md)

