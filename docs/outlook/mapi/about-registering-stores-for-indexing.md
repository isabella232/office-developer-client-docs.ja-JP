---
title: インデックス作成のためのストア登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321827"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="692d6-103">インデックス作成のためのストア登録について</span><span class="sxs-lookup"><span data-stu-id="692d6-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="692d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="692d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="692d6-105">このトピックは、Microsoft Office Outlook 2007 のクイック検索に固有のものです。</span><span class="sxs-lookup"><span data-stu-id="692d6-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="692d6-106">クイック検索を使用すると、Outlook のアイテムをすばやく見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="692d6-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="692d6-107">Windows デスクトップサーチのコンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="692d6-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="692d6-108">MAPI プロトコルハンドラーは、検索用にインデックスが必要なストアの Windows レジストリをチェックします。</span><span class="sxs-lookup"><span data-stu-id="692d6-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="692d6-109">インデックスを作成するストアプロバイダーは、Windows レジストリに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="692d6-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="692d6-110">既定では、windows デスクトップ検索は、次の4種類のストアプロバイダーを windows レジストリに追加して、インデックスを許可します。</span><span class="sxs-lookup"><span data-stu-id="692d6-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="692d6-111">個人用フォルダーファイルのストア (。PST)。</span><span class="sxs-lookup"><span data-stu-id="692d6-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="692d6-112">すべてのオフラインフォルダーファイル (.ost) を含む Microsoft Exchange ストア。</span><span class="sxs-lookup"><span data-stu-id="692d6-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="692d6-113">パブリックフォルダーのストア。</span><span class="sxs-lookup"><span data-stu-id="692d6-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="692d6-114">Microsoft Office Outlook Connector for MSN に保存します。</span><span class="sxs-lookup"><span data-stu-id="692d6-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="692d6-115">インデックスを作成するサードパーティ製のストアプロバイダーは、Windows レジストリに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="692d6-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="692d6-116">管理者とユーザーは、グループポリシー設定を使用して、Windows デスクトップサーチが Outlook アイテムのインデックスを作成できないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="692d6-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="692d6-117">詳細については、「 [Windows デスクトップサーチの拡張](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="692d6-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="692d6-118">レジストリキー</span><span class="sxs-lookup"><span data-stu-id="692d6-118">Registry Keys</span></span>

<span data-ttu-id="692d6-119">コンピューターでは、インデックスを作成するすべてのストアプロバイダーは、Windows レジストリ内の次の3つのレジストリキーのいずれか1つにのみ登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="692d6-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="692d6-120">MAPI プロトコルハンドラーは、次の順序で各キーの下を調べます。</span><span class="sxs-lookup"><span data-stu-id="692d6-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="692d6-121">[HKLM] \Software\Policies\Microsoft\Windows\Windows Search \\</span><span class="sxs-lookup"><span data-stu-id="692d6-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="692d6-122">[HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="692d6-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="692d6-123">[HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="692d6-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="692d6-124">キーの下の各値は、インデックスを作成するストアプロバイダーに対応しています。</span><span class="sxs-lookup"><span data-stu-id="692d6-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="692d6-125">値の名前は、格納プロバイダーのグローバル一意識別子 (GUID) です。これは、 **DWORD**型で、16進数の値0x00000001 です。</span><span class="sxs-lookup"><span data-stu-id="692d6-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="692d6-126">ストアプロバイダーの guid</span><span class="sxs-lookup"><span data-stu-id="692d6-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="692d6-127">mapi プロパティ**[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** は、mapi ストアの GUID を指定します。</span><span class="sxs-lookup"><span data-stu-id="692d6-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="692d6-128">次の表では、Outlook インデックスが格納されているストアプロバイダーの guid について説明します。</span><span class="sxs-lookup"><span data-stu-id="692d6-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="692d6-129">**ストアプロバイダーの種類**</span><span class="sxs-lookup"><span data-stu-id="692d6-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="692d6-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="692d6-130">**GUID**</span></span> <br/> |<span data-ttu-id="692d6-131">**メモ**</span><span class="sxs-lookup"><span data-stu-id="692d6-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="692d6-132">個人用フォルダーファイル (。PST</span><span class="sxs-lookup"><span data-stu-id="692d6-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="692d6-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="692d6-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="692d6-134">GUID は、 **MSPST_UID_PROVIDER**として、パブリックヘッダーファイル mspst に記載されています。</span><span class="sxs-lookup"><span data-stu-id="692d6-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="692d6-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="692d6-135">Exchange</span></span>  <br/> |<span data-ttu-id="692d6-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="692d6-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="692d6-137">guid は、パブリックヘッダーファイル edkmdb で、 **pbexchangeproviderprimaryuserguid**としてドキュメント化されています。</span><span class="sxs-lookup"><span data-stu-id="692d6-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="692d6-138">パブリック フォルダー</span><span class="sxs-lookup"><span data-stu-id="692d6-138">Public folders</span></span>  <br/> |<span data-ttu-id="692d6-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="692d6-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="692d6-140">GUID は、パブリックヘッダーファイル edkmdb では**pbexchangeproviderpublicguid**として記述されています。</span><span class="sxs-lookup"><span data-stu-id="692d6-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="692d6-141">MSN 用 Outlook コネクタ</span><span class="sxs-lookup"><span data-stu-id="692d6-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="692d6-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="692d6-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="692d6-143">なし</span><span class="sxs-lookup"><span data-stu-id="692d6-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="692d6-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="692d6-144">See also</span></span>



[<span data-ttu-id="692d6-145">ストア API について</span><span class="sxs-lookup"><span data-stu-id="692d6-145">About the Store API</span></span>](about-the-store-api.md)

